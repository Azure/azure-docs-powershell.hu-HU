---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838559"
---
# <span data-ttu-id="45bca-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="45bca-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="45bca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45bca-102">SYNOPSIS</span></span>
<span data-ttu-id="45bca-103">Létrehoz egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához.</span><span class="sxs-lookup"><span data-stu-id="45bca-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="45bca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45bca-104">SYNTAX</span></span>

### <span data-ttu-id="45bca-105">AzureToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45bca-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45bca-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="45bca-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45bca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45bca-107">DESCRIPTION</span></span>
<span data-ttu-id="45bca-108">Létrehoz egy olyan lemezkezelő-objektumot, amely egy Azure Virtual Machine-merevlemezt rendel a gyorsítótár-tároló fiókhoz és a TARGET Storage (helyreállítási régió) fiókhoz, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="45bca-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="45bca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="45bca-109">EXAMPLES</span></span>

### <span data-ttu-id="45bca-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45bca-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="45bca-111">Létrehozhat egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához. Az Azure-ban az Azure EnableD és a ReProTect műveletben használatos.</span><span class="sxs-lookup"><span data-stu-id="45bca-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="45bca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45bca-112">PARAMETERS</span></span>

### <span data-ttu-id="45bca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bca-113">-DefaultProfile</span></span>
<span data-ttu-id="45bca-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45bca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45bca-115">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="45bca-115">-DiskId</span></span>
<span data-ttu-id="45bca-116">A felügyelt lemez lemezvezérlő-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="45bca-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="45bca-117">-LogStorageAccountId</span></span>
<span data-ttu-id="45bca-118">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="45bca-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="45bca-119">-ManagedDisk</span></span>
<span data-ttu-id="45bca-120">Itt adhatja meg, hogy a rendszer a kezelt lemez bemenetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="45bca-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="45bca-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="45bca-122">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="45bca-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="45bca-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="45bca-124">A replikált távtárolású lemez fiókjának típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="45bca-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="45bca-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="45bca-126">A replikált távtárolású lemez helyreállítási erőforráscsoport-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="45bca-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="45bca-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="45bca-128">A replikált távtárolású lemez helyreállítási célhelyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45bca-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="45bca-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="45bca-129">-VhdUri</span></span>
<span data-ttu-id="45bca-130">Adja meg annak a lemeznek a VHD-URI-jét, amelyre a megfeleltetés megfelel.</span><span class="sxs-lookup"><span data-stu-id="45bca-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="45bca-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45bca-131">-Confirm</span></span>
<span data-ttu-id="45bca-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45bca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45bca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bca-133">-WhatIf</span></span>
<span data-ttu-id="45bca-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45bca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bca-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45bca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45bca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bca-136">CommonParameters</span></span>
<span data-ttu-id="45bca-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45bca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bca-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bca-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45bca-139">INPUTS</span></span>

### <span data-ttu-id="45bca-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="45bca-140">None</span></span>

## <span data-ttu-id="45bca-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45bca-141">OUTPUTS</span></span>

### <span data-ttu-id="45bca-142">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="45bca-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="45bca-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45bca-143">NOTES</span></span>

## <span data-ttu-id="45bca-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45bca-144">RELATED LINKS</span></span>
