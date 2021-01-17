---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478289"
---
# <span data-ttu-id="18e80-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="18e80-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="18e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18e80-102">SYNOPSIS</span></span>
<span data-ttu-id="18e80-103">Hozzáad egy alkalmazást a megadott Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="18e80-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="18e80-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18e80-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18e80-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18e80-105">DESCRIPTION</span></span>
<span data-ttu-id="18e80-106">A **New-AzBatchApplication** parancsmag hozzáad egy alkalmazást a megadott Azure Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="18e80-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="18e80-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18e80-107">EXAMPLES</span></span>

### <span data-ttu-id="18e80-108">1. példa: Üres alkalmazás hozzáadása kötegfiókhoz</span><span class="sxs-lookup"><span data-stu-id="18e80-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="18e80-109">Ez a parancs létrehozza a Litware alkalmazást a ContosoBatch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="18e80-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="18e80-110">Az alkalmazás kezdetben nem tartalmaz csomagokat.</span><span class="sxs-lookup"><span data-stu-id="18e80-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="18e80-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18e80-111">PARAMETERS</span></span>

### <span data-ttu-id="18e80-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18e80-112">-AccountName</span></span>
<span data-ttu-id="18e80-113">Annak a Batch-fióknak a nevét adja meg, amelyhez ez a parancsmag hozzáad egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="18e80-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="18e80-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="18e80-114">-AllowUpdates</span></span>
<span data-ttu-id="18e80-115">Azt adja meg, hogy az alkalmazáson belüli csomagok felülírhatók-e ugyanazokkal a verziós karakterláncokkal.</span><span class="sxs-lookup"><span data-stu-id="18e80-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e80-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="18e80-116">-ApplicationName</span></span>
<span data-ttu-id="18e80-117">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e80-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="18e80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e80-118">-DefaultProfile</span></span>
<span data-ttu-id="18e80-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18e80-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e80-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="18e80-120">-DisplayName</span></span>
<span data-ttu-id="18e80-121">Az alkalmazás megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e80-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e80-122">-ResourceGroupName</span></span>
<span data-ttu-id="18e80-123">A Batch-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e80-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="18e80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e80-124">CommonParameters</span></span>
<span data-ttu-id="18e80-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e80-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18e80-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e80-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18e80-127">INPUTS</span></span>

### <span data-ttu-id="18e80-128">System.String</span><span class="sxs-lookup"><span data-stu-id="18e80-128">System.String</span></span>

### <span data-ttu-id="18e80-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="18e80-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="18e80-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e80-130">OUTPUTS</span></span>

### <span data-ttu-id="18e80-131">Microsoft.Azure.Commands.Bat. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="18e80-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="18e80-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18e80-132">NOTES</span></span>

## <span data-ttu-id="18e80-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18e80-133">RELATED LINKS</span></span>

[<span data-ttu-id="18e80-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="18e80-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="18e80-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="18e80-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="18e80-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="18e80-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="18e80-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="18e80-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="18e80-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="18e80-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="18e80-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="18e80-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


