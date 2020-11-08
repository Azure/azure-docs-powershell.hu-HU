---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012686"
---
# <span data-ttu-id="8921f-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="8921f-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="8921f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8921f-102">SYNOPSIS</span></span>
<span data-ttu-id="8921f-103">Létrehoz egy olyan ASR-adapter-konfigurációt, amely tartalmazza a feladatátvételi és tesztelési feladatátvételi információkat.</span><span class="sxs-lookup"><span data-stu-id="8921f-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="8921f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8921f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8921f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8921f-105">DESCRIPTION</span></span>
<span data-ttu-id="8921f-106">A **New-AzRecoveryServicesAsrVMNicConfig** parancsmag létrehoz egy ASR-hálózati konfigurációs objektumot, amely tartalmazza a feladatátvételi és tesztelési feladatátvételsel kapcsolatos részleteket.</span><span class="sxs-lookup"><span data-stu-id="8921f-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="8921f-107">Abban az esetben, ha nem történik meg az információk átadása, a megfelelő értékek a replikációs védelemmel ellátott elemből kerülnek, így elkerülhető, hogy ezek az értékek ne legyenek NULL értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="8921f-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="8921f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8921f-108">EXAMPLES</span></span>

### <span data-ttu-id="8921f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8921f-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="8921f-110">Létrehoz egy ASRVmNicConfig objektumot, amelyen a hálózati ADAPTERhez konfigurált feladatátvételi és tesztelési faiover hálózati beállítások láthatók.</span><span class="sxs-lookup"><span data-stu-id="8921f-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="8921f-111">A fentiekben nem átadott tulajdonságokat a program letölti a védett elemből.</span><span class="sxs-lookup"><span data-stu-id="8921f-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="8921f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8921f-112">PARAMETERS</span></span>

### <span data-ttu-id="8921f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8921f-113">-DefaultProfile</span></span>
<span data-ttu-id="8921f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8921f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8921f-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="8921f-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="8921f-116">Meghatározza, hogy engedélyezve van-e a gyorsított hálózat a helyreállítási NIC-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8921f-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="8921f-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="8921f-118">Meghatározza, hogy a gyorsított hálózat engedélyezve van-e a teszt-feladatátvételi NIC-ben.</span><span class="sxs-lookup"><span data-stu-id="8921f-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="8921f-119">-NicI</span><span class="sxs-lookup"><span data-stu-id="8921f-119">-NicId</span></span>
<span data-ttu-id="8921f-120">Adja meg az ASR-adapter GUID-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8921f-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="8921f-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8921f-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="8921f-122">A backend-címkészlet azonosítóit adja meg a helyreállítási hálózati adapterhez.</span><span class="sxs-lookup"><span data-stu-id="8921f-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8921f-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="8921f-124">A helyreállítási hálózati adapterhez társított NSG AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8921f-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="8921f-126">A helyreállítási NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="8921f-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="8921f-128">A helyreállítási NIC-hez társított nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8921f-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="8921f-130">A helyreállítási virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="8921f-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="8921f-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="8921f-132">A helyreállítási alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="8921f-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8921f-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8921f-134">Adja meg az ASR replikációs szolgáltatással védett elemét.</span><span class="sxs-lookup"><span data-stu-id="8921f-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="8921f-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8921f-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="8921f-136">A backend-címkészlet azonosítóit adja meg a helyreállítási hálózati adapterhez.</span><span class="sxs-lookup"><span data-stu-id="8921f-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="8921f-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8921f-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="8921f-138">A teszt-feladatátvételi KÁRTYÁval társított NSG AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="8921f-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="8921f-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="8921f-140">A teszt-feladatátvételi NIC IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="8921f-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="8921f-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="8921f-142">Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amely a teszt feladatátvételi ADAPTERhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="8921f-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="8921f-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8921f-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="8921f-144">A teszt-feladatátvételi virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="8921f-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="8921f-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="8921f-146">A teszt-feladatátvételi alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8921f-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="8921f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8921f-147">CommonParameters</span></span>
<span data-ttu-id="8921f-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8921f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8921f-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8921f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8921f-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8921f-150">INPUTS</span></span>

### <span data-ttu-id="8921f-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="8921f-151">None</span></span>

## <span data-ttu-id="8921f-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8921f-152">OUTPUTS</span></span>

### <span data-ttu-id="8921f-153">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="8921f-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="8921f-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8921f-154">NOTES</span></span>

## <span data-ttu-id="8921f-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8921f-155">RELATED LINKS</span></span>
