---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 97e10d75d17748f1a9e96ada498afe456700f61d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836743"
---
# New-AzVmss

## Áttekintés
Létrehoz egy VMSS.

## SZINTAXISA

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
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzVmss** parancsmag létrehoz egy virtuálisgép-készletet (VMSS) az Azure-ban.
Az egyszerű típusparaméter ( `SimpleParameterSet` ) segítségével gyorsan létrehozhat előre beállított VMSS és kapcsolódó erőforrásokat. Az alapértelmezett paramétert () akkor használja, `DefaultParameter` Ha a VMSS és a hozzájuk rendelt erőforrások mindegyik összetevőjének pontos konfigurálására van szükség a létrehozás előtt.

## Példák

### Példa 1: VMSS létrehozása a **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

A fenti parancs a következőképpen hozza létre a nevet `$vmssName` :
* Erőforráscsoport
* Virtuális hálózat
* A terheléselosztó
* Nyilvános IP-cím
* a VMSS két példányban

A VMSS a VMs-rendszerhez kiválasztott alapértelmezett kép `2016-Datacenter Windows Server` és a SKU `Standard_DS1_v2`

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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
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

A fenti komplex példa létrehoz egy VMSS, az alábbi magyarázattal a mi történik:
* Az első parancs létrehoz egy erőforráscsoportot a megadott névvel és hellyel.
* A második parancs a **New-AzStorageAccount** parancsmagot használja a tárolási fiók létrehozásához.
* A harmadik parancs ezt követően a **Get-AzStorageAccount** parancsmagot használja a második parancsban létrehozott tárterület-fiók beszerzéséhez, és az eredményt a $STOAccount változóban tárolja.
* Az ötödik parancs a **New-AzVirtualNetworkSubnetConfig** parancsmagot használja alhálózat létrehozásához, és az eredményt az $SubNet nevű változóban tárolja.
* A hatodik parancs a **New-AzVirtualNetwork** parancsmagot használja virtuális hálózat létrehozásához, és az eredményt az $VNet nevű változóban tárolja.
* A hetedik parancs a **Get-AzVirtualNetwork** használatával információkat kaphat a hatodik parancsban létrehozott virtuális hálózatról, és az adatokat a $VNet nevű változóban tárolja.
* A nyolcadik és a kilencedik parancs a **New-AzPublicIpAddress** és a **Get-AzureRmPublicIpAddress** használatával hozza létre és kapja meg az adott nyilvános IP-címről származó információkat.
* A parancsok a $PubIP nevű változóban tárolják az adatokat.
* A tizedik parancs a **New-AzureRmLoadBalancerFrontendIpConfig** parancsmagot használja egy frontend terheléselosztás létrehozásához, és az eredményt az $frontend nevű változóban tárolja.
* A tizenegyedik parancs a **New-AzLoadBalancerBackendAddressPoolConfig** segítségével hozza létre a backend-címkészlet konfigurációját, és az eredményt az $BackendAddressPool nevű változóban tárolja.
* A tizenkettedik parancs a **New-AzLoadBalancerProbeConfig** használatával létrehoz egy szondát, és a szonda adatait a $Probe nevű változóban tárolja.
* A tizenharmadik parancs a **New-AzLoadBalancerInboundNatPoolConfig** parancsmagot használja a terheléselosztó bejövő hálózati címfordítási (NAT) alkalmazáskészlet-konfiguráció létrehozásához.
* A tizennegyedik parancs a **New-AzLoadBalancerRuleConfig** segítségével hoz létre terheléselosztó szabály-konfigurációt, és az eredményt az $LBRule nevű változóban tárolja.
* A tizenötödik parancs a **New-AzLoadBalancer** parancsmagot használja a terheléselosztó létrehozásához, és az eredményt az $ActualLb nevű változóban tárolja.
* A tizenhatodik parancs a **Get-AzLoadBalancer** használatával információkat kaphat a tizenötödik parancsban létrehozott terheléselosztó rendszerről, és az adatokat a $ExpectedLb nevű változóban tárolja.
* A tizenhetedik parancs a **New-AzVmssIPConfig** parancsmagot használja a VMSS IP-konfigurációjának létrehozásához, és az adatokat a $IPCfg nevű változóban tárolja.
* A XVIII parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.
* A tizenkilencedik parancs a **New-AzVmss** parancsmagot használja a VMSS létrehozásához.

## PARAMÉTEREK

### -AllocationMethod
A méretarány (statikus vagy dinamikus) nyilvános IP-címének kiosztási módja.  Ha nincs megadva érték, akkor a felosztás statikus lesz.

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
Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.

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
Annak a backend-címkészlet a neve, amelyet az ehhez a léptékhez tartozó terheléselosztásban szeretne használni.  Ha nincs megadva érték, akkor létrejön egy új backend-készlet, amelynek a neve megegyezik a méretarány beállítással.

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
A kiegyenlítő terheléselosztás által a VM-tel való kommunikációhoz a méretarány beállítása által használt backend-portok száma.  Ha nincs megadva érték, akkor a rendszer a 3389 és az 5985-es portot fogja használni a Windows VMS rendszerhez, és a 22-ös portot fogja használni a Linux VM-hez.

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
A virtuális VMs-rendszerhez tartozó rendszergazdai hitelesítő adatok (Felhasználónév és jelszó) ebben a méretarányban jelennek meg.

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
Az adatlemezek méretét adja meg GB-ban.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A nyilvános Fully-Qualified tartománynév címkéje (FQDN) ehhez a méretarányhoz. Ez a tartománynév első olyan része, amelyet a program automatikusan hozzárendel a méretarányhoz. Automatikusan hozzárendelt tartománynevek: használja az űrlapot ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Ha nincs megadva érték, az alapértelmezett tartománynév-címke lesz az ÖSSZEFŰZ <ScaleSetName> és a <ResourceGroupName> .

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
A UltraSSD-lemezek használata a virtuális VMs-rendszerhez a méretarány készletében

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

### -FrontendPoolName
A Scale set terheléselosztó bővítményben használandó felületi címkészlet neve.  Ha nincs megadva érték, akkor létrejön egy új felületi címkészlet, amelynek a neve megegyezik a méretarány beállítással.

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

### -ImageName
A virtuális VM-fájl neve ebben a méretarányban. Ha nincs megadva érték, a program a "Windows Server 2016-adatközpont" képet fogja használni.

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
A virtuális VM-képek száma a méretarányban.  Ha nincs megadva érték, akkor két példány jön létre.

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
Az ezzel a Méretaránysal használandó terheléselosztó neve.  Új terheléselosztó a méretarány nevének megadásával, ha a program nem ad meg értéket.

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

### -Hely
Az Azure-hely, ahol ez a méretarány jön létre.  Ha nincs megadva érték, a program a paraméterben hivatkozott további források helyétől kikövetkezteti a helyet.

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

### -NatBackendPort
A bejövő hálózati címfordításhoz tartozó backend port.

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

### -PublicIpAddressName
Annak a nyilvános IP-címnek a neve, amellyel az adott méretarányt be szeretné használni.  Ha nincs megadva érték, akkor létrejön egy új nyilvános IP-azonosító a méretarány nevével.

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
A VMSS erőforráscsoport-csoportjának nevét adja meg.  Ha nincs megadva érték, új ResourceGroup fog létrejönni a méretarány nevével.

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

### -SecurityGroupName
Annak a hálózati biztonsági csoportnak a neve, amelyre alkalmazni szeretné ezt a méretarányt.  Ha nincs megadva érték, akkor létrejön egy alapértelmezett hálózati biztonsági csoport, amelynek a mérete megegyezik a méretarány beállítással.

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
Ezzel a beállítással létrehozhatja a méretarányt egyetlen Elhelyezés csoportban, az alapértelmezett beállítás több csoport

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
Annak az alhálózatnak az előtagja, amelyet a ScaleSet használni fog. Az alapértelmezett alhálózati beállítások (192.168.1.0/24) akkor érvényesek, ha nincs megadva érték.

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
Annak az alhálózatnak a neve, amely az adott méretarányt használja.  Ha nincs megadva érték, akkor létrejön egy új alhálózat a méretarány-készlet nevével.

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
Ha a paraméter megtalálható, akkor a méretarányban a VM (s) a (a) rendszer automatikusan generált felügyelt rendszeridentitást rendel.

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
Ebben a méretarányban a VM-példányokra vonatkozó frissítési házirend üzemmódot adja meg.  A frissítési házirend az automatikus, a manuális vagy a folyamatos frissítést is megadhatja.

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
Annak a felügyelt szolgáltatás-identitásnak a neve, amelyet ki kell osztani a VM (ek) nek a méretarányban.

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
Azt a **VirtualMachineScaleSet** -objektumot adja meg, amely a parancsmag által létrehozott VMSS tulajdonságait tartalmazza.

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
Annak a virtuális hálózatnak a neve, amellyel az adott méretarányt használni szeretné.  Ha nincs megadva érték, akkor létrejön egy új virtuális hálózat, amelynek a neve megegyezik a méretarány-Halmazsal.

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
Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.

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
A megadott méretarányban a VM-példányok mérete.  Ha nincs megadva méret, az alapértelmezett méret (Standard_DS1_v2) lesz használatos.

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
A megadott Méretaránysal használt virtuális hálózathoz tartozó cím előtagja.  Az alapértelmezett virtuális hálózati cím előtag-beállításai (192.168.0.0/16) akkor lesznek használatban, ha nincs megadva érték.

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

### -Zone (zóna)
Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet

### System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

## KIMENETEK

### Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Újraindítás – AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


