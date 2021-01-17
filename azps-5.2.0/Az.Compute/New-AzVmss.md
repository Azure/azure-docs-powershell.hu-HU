---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372636"
---
# New-AzVmss

## SYNOPSIS
VMSS-t hoz létre.

## SZINTAXIS

### DefaultParameter (alapértelmezett)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVmss** parancsmag virtuálisgép-méretarány-készletet (VMSS) hoz létre az Azure-ban.
Az egyszerű paraméterkészlet () segítségével gyorsan létrehozhat előre beállított `SimpleParameterSet` VMSS-eket és kapcsolódó erőforrásokat. Az alapértelmezett paraméterkészletet ( ) akkor használja, ha speciálisabb esetekre van szüksége, amikor a VMSS és az egyes társított erőforrások mindegyik összetevőjét pontosan be kell állítania a létrehozás `DefaultParameter` előtt.

## PÉLDÁK

### 1. példa: VMSS létrehozása a **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

A fenti parancs a következőt hozza létre a következő `$vmssName` névvel:
* Erőforráscsoport
* Virtuális hálózat
* Terheléselosztás
* Nyilvános IP-cím
* A VMSS 2 példánysal

A VMSS-ban a vmss-hez kiválasztott alapértelmezett kép `2016-Datacenter Windows Server` az, a termékváltozat pedig a `Standard_DS1_v2`

### 2. példa: VMSS létrehozása a **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

A fenti összetett példa VMSS-et hoz létre, az alábbiakban látható, hogy mi történik:
* Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és helyről.
* A második parancs a **New-AzStorageAccount** parancsmaggal hoz létre tárfiókot.
* A harmadik parancs ezután a **Get-AzStorageAccount** parancsmag használatával begyűjte a második parancsban létrehozott tárfiókot, és az eredményt a $STOAccount változóban tárolja.
* Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmaggal hoz létre egy alhálózatot, és az eredményt az $SubNet nevű változóban tárolja.
* A hatodik parancs a **New-AzVirtualNetwork** parancsmag használatával hoz létre egy virtuális hálózatot, és az eredményt a $VNet.
* A hetedik parancs a **Get-AzVirtualNetwork** segítségével információkat kap a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat az $VNet változóban tárolja.
* A nyolcadik és a hetedik parancs a **New-AzPublicIpAddress** és **a Get- AzureRmPublicIpAddress** paranccsal hozza létre és szerezze be az információkat az adott nyilvános IP-címről.
* A parancsok az adatokat a $PubIP.
* A tizedik parancs a **New- AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléseloszlító létrehozásához, és az eredményt a $Frontend.
* A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hoz létre egy háttércímkészlet-konfigurációt, és az eredményt a $BackendAddressPool.
* A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** segítségével létrehoz egy tárolót, és tárolja a mentesítési adatokat a $Probe.
* A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmaggal hoz létre terheléselegyenlő bejövő hálózati címfordítási (NAT) készlet-konfigurációt.
* A tizennégyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselegyenlői szabálykonfigurációt, és az eredményt a következő nevű változóban $LBRule.
* A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztás létrehozására, és az eredményt a következő nevű változóban $ActualLb.
* A 15. parancs a **Get-AzLoadBalancer** segítségével információkat kap a tizenötedik parancsban létrehozott terheléselosztásról, és az adatokat az $ExpectedLb változóban tárolja.
* A tizenhét parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfiguráció létrehozásához, és az adatokat a következő nevű változóban $IPCfg.
* A tizennyolc parancs a **New-AzVmssConfig** parancsmagot használja a VMSS konfigurációs objektum létrehozásához, és az eredményt a következő nevű változóban $VMSS.
* A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.

## PARAMETERS

### -AllocationMethod
A méretaránykészlet nyilvános IP-címének terhelési módja (statikus vagy dinamikus).  Ha nem ad meg értéket, a terhelés statikus lesz.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Az ebben a méretkészletben a terheléselosztásban használt háttércímkészlet neve.  Ha nem ad meg értéket, a rendszer létrehoz egy új háttérkészletet, amely neve megegyezik a méretaránykészlet nevével.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
A scale set load balancer által a méretarányos készletben a virtuális gépekkel való kommunikációra használt háttérportszámok.  Ha nincs megadva érték, a Windows VMS-hez a 3389-es és az 5985-ös portot, Linuxos VMS-hez pedig a 22-es portot fogja használni.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítő adatok
A rendszergazdai hitelesítő adatok (felhasználónév és jelszó) a virtuális gépekhez ebben a méretkészletben.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Az adatlemezek mérete GB-ban.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
A nyilvános tartománynév tartománynevének Fully-Qualified tartománynév (FQDN) a méretaránykészlethez. Ez a tartománynév első olyan összetevője, amely automatikusan hozzá van rendelve a méretskálakészlethez. Az automatikusan hozzárendelt tartománynevek a ( . ) űrlapot <DomainNameLabel> <Location> használják. cloudapp.azure.com) Ha nem ad meg értéket, az alapértelmezett tartománynévfelirat az és. <ScaleSetName> <ResourceGroupName>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltraSSD
Az UltraSSD-lemezeket használhatja a virtuális gépekhez a méretaránykészletben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Ez a paraméter engedélyezi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is. Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforrásra nézve.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EvictionPolicy
Az alacsony prioritású virtuális gép méretarányának beállítását kiviction házirend.  Csak a "Deallocate" és a "Delete" érték támogatott.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Az előlapi címkészlet neve, amely a Scale Set terheléselosztásban használható.  Ha nem ad meg értéket, létrejön egy új előlapi címkészlet, amely a méretaránykészlet nevével azonos.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostGroupId
Megadja azt a dedikált állomáscsoportot, ahol a virtuális gép méretaránykészlete található.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ImageName
A virtuális gépek képének neve ebben a méretkészletben. Ha nem ad meg értéket, a rendszer a "Windows Server 2016 DataCenter" képet használja.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
A VM-képek száma a méretaránykészletben.  Ha nem ad meg értéket, a program 2 példányt hoz létre.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Az ezzel a méretkészletgel használható terheléselosztási rendszer neve.  Ha nincs megadva érték, létrejön egy új terheléselosztási eszköz a méretarányos készlet nevével.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Az Azure-hely, ahol ez a méretaránykészlet létrejön.  Ha nincs megadva érték, a hely a paraméterekben hivatkozott egyéb erőforrások helyéről lesz kikövetkeztetve.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Egy alacsony prioritású virtuálisgép-méretarányú készlet számlázásának maximális ára.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Backend port inbound network address translation.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
A hibatartományok száma az egyes elhelyezési csoportoknál.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
A virtuális gép prioritása a méretaránykészletben.  Csak a "Normál", a "Direkt" és az "Alacsony" támogatott értékek támogatottak.
A "Regular" normál virtuális géphez való.
A "Spot" a direkt virtuális gépekhez való.
A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli. Használja a "Spot" (Direkt) használhatja az "Alacsony" helyett.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Az ezzel a méretkészlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Az ezzel a méretkészletet használva használt nyilvános IP-cím neve.  Ha nem ad meg értéket, a rendszer létrehoz egy új nyilvános IPAddress címet, a méretaránykészlet nevével.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A VMSS erőforráscsoport nevét adja meg.  Ha nincs megadva érték, a méretaránykészlet nevével egy új Erőforráscsoport jön létre.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
A virtuális gép méretarányának beállításakor be kell tartani a szabályokat.  Lehetséges értékek: "Alapértelmezett", "LegrégebbiVM" és "LegújabbVM".  Az "Alapértelmezett" érték a virtuális gép méretarány-készletének méretaránya esetén először a zónák között lesz kiegyensúlyozott, ha az egy állatövi méretarányú készlet.  Ezt követően lehetőség szerint kiegyensúlyozott lesz a hibatartományok között.  Az egyes hibatartományok esetén az eltávolításhoz kiválasztott virtuális gépek lesznek a legújabbak, amelyek nem védettek a méretaránytól.  A "oldestVM" akkor lesz kiválasztva eltávolításra, ha méretarányos virtuális gépkészletet ad meg.  Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.  Az egyes zónákban a nem védett legrégebbi virtuális gépek lesznek kiválasztva eltávolításra.  "LegújabbVM", amikor egy virtuális gép méretaránykészletét méretarányosra méretezik, a rendszer kiválasztja a méretaránytól nem védett legújabb virtuális gépeket az eltávolításhoz.  Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.  Az egyes zónákon belül a nem védett legújabb virtuális gépek lesznek kiválasztva eltávolításra.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Az erre a méretaránykészletre alkalmazandó hálózati biztonsági csoport neve.  Ha nincs megjelölve érték, a rendszer létrehoz és alkalmaz egy, a méretaránykészletével azonos nevű alapértelmezett hálózatbiztonsági csoportot.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Ezzel a beállítással egyetlen elhelyezési csoportban hozhatja létre a méretarányt, az alapértelmezett beállítás több csoport.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Azt adja meg, hogy a bővítmények nem futnak túlzsúfolt virtuális gépeken.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
A ScaleSet alhálózat címelőtagja. Ha nem ad meg értéket, az alhálózat alapértelmezett beállításai (192.168.1.0/24) lesznek érvényesek.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Az ezzel a méretaránykészlettel használt alhálózat neve.  Ha nem ad meg értéket, létrejön egy új alhálózat a méretaránykészlettel azonos néven.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Ha a paraméter jelen van, akkor a méretaránykészletBEN található VM(k) egy automatikusan létrehozott felügyelt rendszer-identitáshoz vannak hozzárendelve.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
A vm-példányok frissítési házirendmódja ebben a méretkészletben.  A frissítési házirend megadhatja az automatikus, a manuális és a folyamatos frissítéseket.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Annak a felügyelt szolgáltatás-identitásnak a neve, amely a méretaránykészletben a VM(k)hez van hozzárendelve.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Megadja a **VirtualMachineScaleSet** objektumot, amely a parancsmag által létrehozott VMSS-tulajdonságokat tartalmazza.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Az ezzel a méretkészlethez használt virtuális hálózat neve.  Ha nem ad meg értéket, létrejön egy új virtuális hálózat a méretaránykészlet nevével.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
A parancsmag által létrehozott VMSS-nek a neve.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
A VM-példányok mérete ebben a méretkészletben.  Alapértelmezett méret (Standard_DS1_v2) fog használni, ha nincs megadva méret.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
A méretaránykészlethez használt virtuális hálózat címelőtagja.  Ha nem ad meg értéket, a virtuális hálózat címének előtagbeállítása (192.168.0.0/16) lesz használatos.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
A rendelkezésre állási zónák listája, amely az erőforráshoz kiosztott IP-címet sorolja fel.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVms](./Get-AzVmss.md)

[Remove-AzVms](./Remove-AzVmss.md)

[Restart-AzVms](./Restart-AzVmss.md)

[Set-AzVms](./Set-AzVmss.md)

[Start-AzVms](./Start-AzVmss.md)

[Stop-AzVms](./Stop-AzVmss.md)

[Update-AzVms](./Update-AzVmss.md)


