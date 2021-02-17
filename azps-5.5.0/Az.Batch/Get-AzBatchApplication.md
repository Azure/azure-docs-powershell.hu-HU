---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205350"
---
# <span data-ttu-id="e0b4d-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e0b4d-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="e0b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b4d-103">Információt kap a megadott alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="e0b4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0b4d-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b4d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b4d-106">A **Get-AzBatchApplication** parancsmag információt kap egy Azure Batch-fiókban található alkalmazásról.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="e0b4d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b4d-108">1. példa: Az alkalmazások megjelenítése egy Batch-fiókban</span><span class="sxs-lookup"><span data-stu-id="e0b4d-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="e0b4d-109">Ez a parancs megjeleníti a ContosoBatch-fiók összes alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="e0b4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b4d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0b4d-111">-AccountName</span></span>
<span data-ttu-id="e0b4d-112">Az alkalmazást tartalmazó Batch-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="e0b4d-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e0b4d-113">-ApplicationName</span></span>
<span data-ttu-id="e0b4d-114">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b4d-115">-DefaultProfile</span></span>
<span data-ttu-id="e0b4d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0b4d-118">A Batch-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e0b4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b4d-119">CommonParameters</span></span>
<span data-ttu-id="e0b4d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b4d-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b4d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0b4d-122">INPUTS</span></span>

### <span data-ttu-id="e0b4d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e0b4d-123">System.String</span></span>

## <span data-ttu-id="e0b4d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b4d-124">OUTPUTS</span></span>

### <span data-ttu-id="e0b4d-125">Microsoft.Azure.Commands.Bat. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="e0b4d-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="e0b4d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0b4d-126">NOTES</span></span>

## <span data-ttu-id="e0b4d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0b4d-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0b4d-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e0b4d-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e0b4d-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e0b4d-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e0b4d-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e0b4d-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e0b4d-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e0b4d-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e0b4d-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e0b4d-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e0b4d-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e0b4d-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


