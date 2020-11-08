---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184263"
---
# <span data-ttu-id="fe259-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="fe259-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="fe259-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe259-102">SYNOPSIS</span></span>
<span data-ttu-id="fe259-103">Létrehoz egy olyan ASR-adapter-konfigurációt, amely tartalmazza a feladatátvételi és tesztelési feladatátvételi információkat.</span><span class="sxs-lookup"><span data-stu-id="fe259-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="fe259-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe259-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe259-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe259-105">DESCRIPTION</span></span>
<span data-ttu-id="fe259-106">A **New-AzRecoveryServicesAsrVMNicConfig** parancsmag létrehoz egy ASR-hálózati konfigurációs objektumot, amely tartalmazza a feladatátvételi és tesztelési feladatátvételsel kapcsolatos részleteket.</span><span class="sxs-lookup"><span data-stu-id="fe259-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="fe259-107">Abban az esetben, ha nem történik meg az információk átadása, a megfelelő értékek a replikációs védelemmel ellátott elemből kerülnek, így elkerülhető, hogy ezek az értékek ne legyenek NULL értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="fe259-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="fe259-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe259-108">EXAMPLES</span></span>

### <span data-ttu-id="fe259-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe259-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="fe259-110">Létrehoz egy ASRVmNicConfig objektumot, amelyen a hálózati ADAPTERhez konfigurált feladatátvételi és tesztelési faiover hálózati beállítások láthatók.</span><span class="sxs-lookup"><span data-stu-id="fe259-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="fe259-111">A fentiekben nem átadott tulajdonságokat a program letölti a védett elemből.</span><span class="sxs-lookup"><span data-stu-id="fe259-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="fe259-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fe259-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="fe259-113">Létrehoz egy ASRVmNicConfig objektumot a hálózati adapterhez beállított faiover hálózati beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="fe259-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="fe259-114">A fentiekben nem átadott tulajdonságokat a program letölti a védett elemből.</span><span class="sxs-lookup"><span data-stu-id="fe259-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="fe259-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fe259-115">Example 3</span></span>

<span data-ttu-id="fe259-116">Létrehoz egy olyan ASR-adapter-konfigurációt, amely tartalmazza a feladatátvételi és tesztelési feladatátvételi információkat.</span><span class="sxs-lookup"><span data-stu-id="fe259-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="fe259-117">autogenerated</span><span class="sxs-lookup"><span data-stu-id="fe259-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="fe259-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe259-118">PARAMETERS</span></span>

### <span data-ttu-id="fe259-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe259-119">-DefaultProfile</span></span>
<span data-ttu-id="fe259-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe259-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe259-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="fe259-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="fe259-122">Meghatározza, hogy engedélyezve van-e a gyorsított hálózat a helyreállítási NIC-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="fe259-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="fe259-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="fe259-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="fe259-124">Meghatározza, hogy a gyorsított hálózat engedélyezve van-e a teszt-feladatátvételi NIC-ben.</span><span class="sxs-lookup"><span data-stu-id="fe259-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="fe259-125">-NicI</span><span class="sxs-lookup"><span data-stu-id="fe259-125">-NicId</span></span>
<span data-ttu-id="fe259-126">Adja meg az ASR-adapter GUID-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="fe259-126">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fe259-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="fe259-128">A backend-címkészlet azonosítóit adja meg a helyreállítási hálózati adapterhez.</span><span class="sxs-lookup"><span data-stu-id="fe259-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fe259-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="fe259-130">A helyreállítási hálózati adapterhez társított NSG AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="fe259-131">-RecoveryNicName</span></span>
<span data-ttu-id="fe259-132">A helyreállítási adapter nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-132">Specifies the name of the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe259-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="fe259-134">A helyreállítási NIC erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-134">Specifies the name of the recovery NIC resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="fe259-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="fe259-136">A helyreállítási NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-136">Specifies the IP address of the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fe259-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="fe259-138">A helyreállítási NIC-hez társított nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fe259-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="fe259-140">A helyreállítási virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-140">Specifies the ID of the recovery virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="fe259-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="fe259-142">A helyreállítási alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-142">Specifies the name of the recovery subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe259-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fe259-144">Adja meg az ASR replikációs szolgáltatással védett elemét.</span><span class="sxs-lookup"><span data-stu-id="fe259-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="fe259-145">-ReuseExistingNic</span></span>
<span data-ttu-id="fe259-146">Megadja, hogy a meglévő hálózati adapter használható-e a feladatátvétel során.</span><span class="sxs-lookup"><span data-stu-id="fe259-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="fe259-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fe259-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="fe259-148">A backend-címkészlet azonosítóit adja meg a helyreállítási hálózati adapterhez.</span><span class="sxs-lookup"><span data-stu-id="fe259-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fe259-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="fe259-150">A teszt-feladatátvételi KÁRTYÁval társított NSG AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="fe259-151">-TfoNicName</span></span>
<span data-ttu-id="fe259-152">A teszt feladatátvételi ADAPTERének neve.</span><span class="sxs-lookup"><span data-stu-id="fe259-152">Specifies the name of the test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe259-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="fe259-154">Itt adhatja meg a feladatátvételi adapter tesztelési erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="fe259-154">Specifies the name of the test failover NIC resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="fe259-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="fe259-156">A teszt-feladatátvételi NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-156">Specifies the IP address of the test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fe259-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="fe259-158">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amely a teszt feladatátvételi ADAPTERhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="fe259-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="fe259-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="fe259-160">Azt adja meg, hogy a teszt feladatátvétele során használható-e meglévő hálózati adapter.</span><span class="sxs-lookup"><span data-stu-id="fe259-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="fe259-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fe259-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="fe259-162">A teszt-feladatátvételi virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-162">Specifies the ID of the test failover virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="fe259-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="fe259-164">A teszt-feladatátvételi alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe259-164">Specifies the name of the test failover subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe259-165">-Confirm</span></span>
<span data-ttu-id="fe259-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe259-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe259-167">-WhatIf</span></span>
<span data-ttu-id="fe259-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe259-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe259-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe259-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe259-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe259-170">CommonParameters</span></span>
<span data-ttu-id="fe259-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe259-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe259-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe259-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe259-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe259-173">INPUTS</span></span>

### <span data-ttu-id="fe259-174">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe259-174">None</span></span>

## <span data-ttu-id="fe259-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe259-175">OUTPUTS</span></span>

### <span data-ttu-id="fe259-176">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="fe259-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="fe259-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe259-177">NOTES</span></span>

## <span data-ttu-id="fe259-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe259-178">RELATED LINKS</span></span>
