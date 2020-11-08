---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194189"
---
# <span data-ttu-id="1abab-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="1abab-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1abab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1abab-102">SYNOPSIS</span></span>
<span data-ttu-id="1abab-103">Létrehoz egy lemezkezelő-objektumot a vMWare Virtual Machine-lemezek replikálásához.</span><span class="sxs-lookup"><span data-stu-id="1abab-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="1abab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1abab-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1abab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1abab-105">DESCRIPTION</span></span>
<span data-ttu-id="1abab-106">Létrehoz egy olyan lemezkezelő-objektumot, amely egy vMWare Virtual Machine-merevlemezt rendel a gyorsítótár-tárterület-fiókhoz, és a cél felügyelt lemez típusa (helyreállítási terület) segítségével replikálja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="1abab-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="1abab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1abab-107">EXAMPLES</span></span>

### <span data-ttu-id="1abab-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1abab-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="1abab-109">Hozzon létre egy lemezkezelő-objektumot a vMWare Virtual Machine-lemezek replikálásához. A vMWare Machine védelem engedélyezésekor használatos.</span><span class="sxs-lookup"><span data-stu-id="1abab-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="1abab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1abab-110">PARAMETERS</span></span>

### <span data-ttu-id="1abab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abab-111">-DefaultProfile</span></span>
<span data-ttu-id="1abab-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1abab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1abab-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1abab-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1abab-114">A távtárolású lemezek titkosításához használt Lemezkezelés-készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1abab-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="1abab-115">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="1abab-115">-DiskId</span></span>
<span data-ttu-id="1abab-116">Adja meg annak a lemeznek a beosztását, amelyre a megfeleltetés megfelel.</span><span class="sxs-lookup"><span data-stu-id="1abab-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="1abab-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="1abab-117">-DiskType</span></span>
<span data-ttu-id="1abab-118">A helyreállítási lemez típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1abab-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="1abab-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1abab-119">-LogStorageAccountId</span></span>
<span data-ttu-id="1abab-120">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1abab-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="1abab-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1abab-121">-Confirm</span></span>
<span data-ttu-id="1abab-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1abab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1abab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1abab-123">-WhatIf</span></span>
<span data-ttu-id="1abab-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1abab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1abab-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1abab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1abab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abab-126">CommonParameters</span></span>
<span data-ttu-id="1abab-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1abab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abab-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1abab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abab-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1abab-129">INPUTS</span></span>

### <span data-ttu-id="1abab-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="1abab-130">None</span></span>

## <span data-ttu-id="1abab-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1abab-131">OUTPUTS</span></span>

### <span data-ttu-id="1abab-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="1abab-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1abab-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1abab-133">NOTES</span></span>

## <span data-ttu-id="1abab-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1abab-134">RELATED LINKS</span></span>
