---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359545"
---
# <span data-ttu-id="da75e-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="da75e-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="da75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da75e-102">SYNOPSIS</span></span>
<span data-ttu-id="da75e-103">Létrehoz egy ASR NIC-konfigurációt, amely tartalmazza a feladatátvételhez és a feladatátvételhez kapcsolódó konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="da75e-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="da75e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da75e-104">SYNTAX</span></span>

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

## <span data-ttu-id="da75e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da75e-105">DESCRIPTION</span></span>
<span data-ttu-id="da75e-106">A **New-AzRecoveryServicesAsrVMNicConfig** parancsmag létrehoz egy ASR NIC konfigurációs objektumot, amely tartalmazza a feladatátvételhez és a feladatátvételhez kapcsolódó részleteket.</span><span class="sxs-lookup"><span data-stu-id="da75e-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="da75e-107">Ha nem ad át semmilyen információt, a megfelelő értékeket a rendszer a replikációval védett elemből kiveszi, hogy elkerülje az értékek null értékűre frissítését.</span><span class="sxs-lookup"><span data-stu-id="da75e-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="da75e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da75e-108">EXAMPLES</span></span>

### <span data-ttu-id="da75e-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="da75e-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="da75e-110">Létrehoz egy ASRVmNicConfig objektumot a feladatátvételi művelettal, és teszteli a hálózati hálózati beállításokat a NIC-hez konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="da75e-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="da75e-111">Minden olyan tulajdonság, amely nem ad át fentieket, a védett elem által átadott elemből lesz lehívva.</span><span class="sxs-lookup"><span data-stu-id="da75e-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="da75e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="da75e-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="da75e-113">Létrehoz egy ASRVmNicConfig objektumot a NIC-renaminghoz konfigurált hálózati tesztelési beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="da75e-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="da75e-114">Minden olyan tulajdonság, amely nem ad át fentieket, a védett elem által átadott elemből lesz lehívva.</span><span class="sxs-lookup"><span data-stu-id="da75e-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="da75e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="da75e-115">Example 3</span></span>

<span data-ttu-id="da75e-116">Létrehoz egy ASR NIC-konfigurációt, amely tartalmazza a feladatátvételhez és a feladatátvételhez kapcsolódó konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="da75e-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="da75e-117">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="da75e-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="da75e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da75e-118">PARAMETERS</span></span>

### <span data-ttu-id="da75e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da75e-119">-DefaultProfile</span></span>
<span data-ttu-id="da75e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da75e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da75e-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="da75e-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="da75e-122">Azt adja meg, hogy engedélyezve van-e a gyors hálózatépítés a helyreállítási NIC szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="da75e-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="da75e-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="da75e-124">Azt adja meg, hogy engedélyezve van-e a gyorsítás a feladatátvételi NIC teszten.</span><span class="sxs-lookup"><span data-stu-id="da75e-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="da75e-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="da75e-125">-NicId</span></span>
<span data-ttu-id="da75e-126">Adja meg az ASR NIC GUID azonosítót.</span><span class="sxs-lookup"><span data-stu-id="da75e-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="da75e-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da75e-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="da75e-128">A helyreállítási NIC háttér-címkészletének ip-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="da75e-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="da75e-130">A helyreállítási NIC-hez társított NSG azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="da75e-131">-RecoveryNicName</span></span>
<span data-ttu-id="da75e-132">A helyreállítási NIC nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da75e-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="da75e-134">A helyreállítási NIC erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="da75e-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="da75e-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="da75e-136">A helyreállítási NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="da75e-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="da75e-138">A helyreállítási NIC-hez társított nyilvános IP-cím azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="da75e-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="da75e-140">A virtuális helyreállítási hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="da75e-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="da75e-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="da75e-142">A helyreállítási alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="da75e-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da75e-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="da75e-144">Adja meg a asr replikációs védelem alatt alatt következő elemet.</span><span class="sxs-lookup"><span data-stu-id="da75e-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="da75e-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="da75e-145">-ReuseExistingNic</span></span>
<span data-ttu-id="da75e-146">Azt adja meg, hogy használható-e meglévő NIC a feladatátvétel során.</span><span class="sxs-lookup"><span data-stu-id="da75e-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="da75e-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da75e-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="da75e-148">A helyreállítási NIC háttér-címkészletének ip-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="da75e-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="da75e-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="da75e-150">A feladatátvételi NIC teszthez társított NSG azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="da75e-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="da75e-151">-TfoNicName</span></span>
<span data-ttu-id="da75e-152">A teszt feladatátvételi NIC nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="da75e-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da75e-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="da75e-154">A teszt feladatátvételi NIC erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="da75e-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="da75e-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="da75e-156">A teszt feladatátvételi NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="da75e-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="da75e-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="da75e-158">A teszt feladatátvételi NIC-hez társított nyilvános IP-cím azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="da75e-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="da75e-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="da75e-160">Azt adja meg, hogy használható-e meglévő NIC a teszt feladatátvétele során.</span><span class="sxs-lookup"><span data-stu-id="da75e-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="da75e-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="da75e-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="da75e-162">A teszt feladatátvételi virtuális hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da75e-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="da75e-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="da75e-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="da75e-164">A teszt feladatátvételi alhálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da75e-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="da75e-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da75e-165">-Confirm</span></span>
<span data-ttu-id="da75e-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da75e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da75e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da75e-167">-WhatIf</span></span>
<span data-ttu-id="da75e-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da75e-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da75e-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da75e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da75e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da75e-170">CommonParameters</span></span>
<span data-ttu-id="da75e-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da75e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da75e-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da75e-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da75e-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da75e-173">INPUTS</span></span>

### <span data-ttu-id="da75e-174">Nincs</span><span class="sxs-lookup"><span data-stu-id="da75e-174">None</span></span>

## <span data-ttu-id="da75e-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da75e-175">OUTPUTS</span></span>

### <span data-ttu-id="da75e-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="da75e-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="da75e-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da75e-177">NOTES</span></span>

## <span data-ttu-id="da75e-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da75e-178">RELATED LINKS</span></span>
