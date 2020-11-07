---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672105"
---
# <span data-ttu-id="e5715-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e5715-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e5715-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5715-102">SYNOPSIS</span></span>
<span data-ttu-id="e5715-103">Létrehoz egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához.</span><span class="sxs-lookup"><span data-stu-id="e5715-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5715-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5715-104">SYNTAX</span></span>

### <span data-ttu-id="e5715-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5715-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5715-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e5715-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5715-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5715-107">DESCRIPTION</span></span>
<span data-ttu-id="e5715-108">Létrehoz egy olyan lemezkezelő-objektumot, amely egy Azure Virtual Machine-merevlemezt rendel a gyorsítótár-tároló fiókhoz és a TARGET Storage (helyreállítási régió) fiókhoz, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="e5715-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="e5715-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5715-109">EXAMPLES</span></span>

### <span data-ttu-id="e5715-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e5715-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="e5715-111">Létrehozhat egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához. Az Azure-ban az Azure EnableD és a ReProTect műveletben használatos.</span><span class="sxs-lookup"><span data-stu-id="e5715-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="e5715-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5715-112">PARAMETERS</span></span>

### <span data-ttu-id="e5715-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5715-113">-DefaultProfile</span></span>
<span data-ttu-id="e5715-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5715-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5715-115">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="e5715-115">-DiskId</span></span>
<span data-ttu-id="e5715-116">A felügyelt lemez lemezvezérlő-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e5715-117">-LogStorageAccountId</span></span>
<span data-ttu-id="e5715-118">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="e5715-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e5715-119">-ManagedDisk</span></span>
<span data-ttu-id="e5715-120">Itt adhatja meg, hogy a rendszer a kezelt lemez bemenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e5715-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e5715-122">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e5715-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="e5715-124">A replikált távtárolású lemez fiókjának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e5715-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e5715-126">A replikált távtárolású lemez helyreállítási erőforráscsoport-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e5715-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="e5715-128">A replikált távtárolású lemez helyreállítási célhelyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5715-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e5715-129">-VhdUri</span></span>
<span data-ttu-id="e5715-130">Adja meg annak a lemeznek a VHD-URI-jét, amelyre a megfeleltetés megfelel.</span><span class="sxs-lookup"><span data-stu-id="e5715-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5715-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5715-131">-Confirm</span></span>
<span data-ttu-id="e5715-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5715-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5715-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5715-133">-WhatIf</span></span>
<span data-ttu-id="e5715-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5715-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5715-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5715-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5715-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5715-136">CommonParameters</span></span>
<span data-ttu-id="e5715-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5715-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5715-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5715-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5715-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5715-139">INPUTS</span></span>

### <span data-ttu-id="e5715-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5715-140">None</span></span>

## <span data-ttu-id="e5715-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5715-141">OUTPUTS</span></span>

### <span data-ttu-id="e5715-142">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e5715-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e5715-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5715-143">NOTES</span></span>

## <span data-ttu-id="e5715-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5715-144">RELATED LINKS</span></span>
