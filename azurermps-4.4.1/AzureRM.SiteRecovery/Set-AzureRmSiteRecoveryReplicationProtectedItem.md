---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494645"
---
# <span data-ttu-id="49452-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="49452-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49452-102">SYNOPSIS</span></span>
<span data-ttu-id="49452-103">A helyreállítási tulajdonságokat (például a cél hálózat és a virtuális gép méretét) állítja be a replikációs szolgáltatással védett elemekhez.</span><span class="sxs-lookup"><span data-stu-id="49452-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49452-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49452-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49452-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49452-105">DESCRIPTION</span></span>
<span data-ttu-id="49452-106">A **set-AzureRmSiteRecoveryReplicationProtectedItem** parancsmag a replikációs szolgáltatással védett elemek helyreállítási tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="49452-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="49452-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49452-107">EXAMPLES</span></span>

## <span data-ttu-id="49452-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49452-108">PARAMETERS</span></span>

### <span data-ttu-id="49452-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="49452-109">-LicenseType</span></span>
<span data-ttu-id="49452-110">A Windows Server-alapú virtuális gépekhez a hibrid használat előnyeiből áttelepített licenc típusának kiválasztása.</span><span class="sxs-lookup"><span data-stu-id="49452-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49452-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49452-111">-Name</span></span>
<span data-ttu-id="49452-112">A helyreállítási virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49452-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="49452-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="49452-113">-NicSelectionType</span></span>
<span data-ttu-id="49452-114">A hálózati csatolókártya (NIC) tulajdonságát adja meg a felhasználó által megadott vagy alapértelmezés szerint beállítással.</span><span class="sxs-lookup"><span data-stu-id="49452-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="49452-115">A NotSelected megadásával visszatérhet az alapértelmezett értékekhez.</span><span class="sxs-lookup"><span data-stu-id="49452-115">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49452-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="49452-116">-PrimaryNic</span></span>
<span data-ttu-id="49452-117">Annak a virtuális gépnek a NIC-je, amelyhez a parancsmag a helyreállítási hálózat tulajdonságot állítja be.</span><span class="sxs-lookup"><span data-stu-id="49452-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="49452-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="49452-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="49452-119">Annak az Azure virtuális hálózatnak az AZONOSÍTÓját adja meg, amelyre ez a parancsmag visszanyeri a védett elemet.</span><span class="sxs-lookup"><span data-stu-id="49452-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="49452-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="49452-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="49452-121">Azt a statikus IP-címet adja meg, amelyet az elsődleges NIC-be kell rendelni a helyreállításhoz.</span><span class="sxs-lookup"><span data-stu-id="49452-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="49452-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="49452-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="49452-123">A helyreállítási Azure virtuális hálózatban annak az alhálózatnak a nevét adja meg, amelyre a parancsmag visszanyeri a védett elemet.</span><span class="sxs-lookup"><span data-stu-id="49452-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="49452-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="49452-125">Az Azure webhely-helyreállítási replikációval védett elemét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49452-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49452-126">-Méret</span><span class="sxs-lookup"><span data-stu-id="49452-126">-Size</span></span>
<span data-ttu-id="49452-127">A helyreállítási virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49452-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="49452-128">Az értéknek az Azure Virtual Machines által támogatott méreteknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="49452-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="49452-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49452-129">-DefaultProfile</span></span>
<span data-ttu-id="49452-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49452-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49452-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49452-131">CommonParameters</span></span>
<span data-ttu-id="49452-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49452-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49452-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49452-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49452-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49452-134">INPUTS</span></span>

### <span data-ttu-id="49452-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="49452-136">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="49452-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="49452-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49452-137">OUTPUTS</span></span>

### <span data-ttu-id="49452-138">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="49452-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="49452-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49452-139">NOTES</span></span>

## <span data-ttu-id="49452-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49452-140">RELATED LINKS</span></span>

[<span data-ttu-id="49452-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="49452-142">Új – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="49452-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49452-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
