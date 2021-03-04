---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 857bc438d1c51b28e3ead1095ca4722fce7ccc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921634"
---
# <span data-ttu-id="90511-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="90511-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="90511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90511-102">SYNOPSIS</span></span>
<span data-ttu-id="90511-103">Lemezleképezés objektumot hoz létre a vMWare virtuális számítógép lemezei replikálása során.</span><span class="sxs-lookup"><span data-stu-id="90511-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="90511-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90511-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90511-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90511-105">DESCRIPTION</span></span>
<span data-ttu-id="90511-106">Létrehoz egy lemezmegfeleltetési objektumot, amely leképezi a vMWare virtuális számítógép lemezét a gyorsítótár-tárfiókhoz és a célként kezelt lemeztípushoz (helyreállítási területhez) a lemez replikálására.</span><span class="sxs-lookup"><span data-stu-id="90511-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="90511-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90511-107">EXAMPLES</span></span>

### <span data-ttu-id="90511-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="90511-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="90511-109">Hozzon létre egy lemezleképezési objektumot a vMWare virtuális számítógép lemezei replikálása számára. A vMWare gép védelmének engedélyezése során használatos.</span><span class="sxs-lookup"><span data-stu-id="90511-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="90511-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90511-110">PARAMETERS</span></span>

### <span data-ttu-id="90511-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90511-111">-DefaultProfile</span></span>
<span data-ttu-id="90511-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90511-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90511-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="90511-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="90511-114">A felügyelt lemez titkosítási készletének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90511-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="90511-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="90511-115">-DiskId</span></span>
<span data-ttu-id="90511-116">Adja meg annak a lemeznek a DiskId-ét, amely megfelel a megfeleltetésnek.</span><span class="sxs-lookup"><span data-stu-id="90511-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="90511-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="90511-117">-DiskType</span></span>
<span data-ttu-id="90511-118">A helyreállítási lemez típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="90511-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="90511-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="90511-119">-LogStorageAccountId</span></span>
<span data-ttu-id="90511-120">A replikációs naplók tárolásához használt napló- vagy gyorsítótárfiók-azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="90511-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="90511-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90511-121">-Confirm</span></span>
<span data-ttu-id="90511-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90511-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90511-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90511-123">-WhatIf</span></span>
<span data-ttu-id="90511-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90511-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90511-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90511-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90511-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90511-126">CommonParameters</span></span>
<span data-ttu-id="90511-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90511-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90511-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90511-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90511-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90511-129">INPUTS</span></span>

### <span data-ttu-id="90511-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="90511-130">None</span></span>

## <span data-ttu-id="90511-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90511-131">OUTPUTS</span></span>

### <span data-ttu-id="90511-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="90511-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="90511-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90511-133">NOTES</span></span>

## <span data-ttu-id="90511-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90511-134">RELATED LINKS</span></span>
