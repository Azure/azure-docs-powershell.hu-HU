---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164250"
---
# <span data-ttu-id="f1cc3-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f1cc3-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="f1cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cc3-103">Egy alkalmazáscsomagrekord és a bináris fájl törlése.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="f1cc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1cc3-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1cc3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cc3-106">A **Remove-AzBatchApplicationPackage** parancsmag egy alkalmazáscsomagrekordot és a bináris fájlt töröl egy Azure Batch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="f1cc3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="f1cc3-108">1. példa: Alkalmazáscsomag törlése Egy Batch-fiókból</span><span class="sxs-lookup"><span data-stu-id="f1cc3-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="f1cc3-109">Ez a parancs törli a Litware alkalmazás 1.0-s verzióját a ContosoBatchGroup-fiókból.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="f1cc3-110">A parancs a csomag bináris fájlját tartalmazó csomagrekordot és blobot is törli.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="f1cc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1cc3-111">PARAMETERS</span></span>

### <span data-ttu-id="f1cc3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1cc3-112">-AccountName</span></span>
<span data-ttu-id="f1cc3-113">Annak a Batch-fióknak a nevét adja meg, amelyből a parancsmag töröl egy alkalmazáscsomagot.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cc3-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f1cc3-114">-ApplicationName</span></span>
<span data-ttu-id="f1cc3-115">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cc3-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="f1cc3-116">-ApplicationVersion</span></span>
<span data-ttu-id="f1cc3-117">Az alkalmazás verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cc3-118">-DefaultProfile</span></span>
<span data-ttu-id="f1cc3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cc3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1cc3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1cc3-121">A Batch-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cc3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cc3-122">CommonParameters</span></span>
<span data-ttu-id="f1cc3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cc3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cc3-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1cc3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cc3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1cc3-125">INPUTS</span></span>

### <span data-ttu-id="f1cc3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f1cc3-126">System.String</span></span>

## <span data-ttu-id="f1cc3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1cc3-127">OUTPUTS</span></span>

### <span data-ttu-id="f1cc3-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="f1cc3-128">System.Void</span></span>

## <span data-ttu-id="f1cc3-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1cc3-129">NOTES</span></span>

## <span data-ttu-id="f1cc3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1cc3-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1cc3-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f1cc3-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="f1cc3-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f1cc3-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f1cc3-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f1cc3-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="f1cc3-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f1cc3-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f1cc3-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f1cc3-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="f1cc3-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f1cc3-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


