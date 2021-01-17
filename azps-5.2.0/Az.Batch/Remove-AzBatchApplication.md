---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361267"
---
# <span data-ttu-id="1aaf2-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1aaf2-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="1aaf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaf2-103">Egy alkalmazást töröl egy Batch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="1aaf2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1aaf2-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aaf2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1aaf2-105">DESCRIPTION</span></span>
<span data-ttu-id="1aaf2-106">A **Remove-AzBatchApplication** parancsmag töröl egy alkalmazást egy Azure Batch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="1aaf2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1aaf2-107">EXAMPLES</span></span>

### <span data-ttu-id="1aaf2-108">1. példa: Alkalmazás törlése egy Batch-fiókból</span><span class="sxs-lookup"><span data-stu-id="1aaf2-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="1aaf2-109">Ez a parancs törli a Litware alkalmazást a ContosoBatch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="1aaf2-110">A parancs nem sikerül, ha az alkalmazás csomagokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="1aaf2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aaf2-111">PARAMETERS</span></span>

### <span data-ttu-id="1aaf2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1aaf2-112">-AccountName</span></span>
<span data-ttu-id="1aaf2-113">Annak a Batch-fióknak a nevét adja meg, amelyből a parancsmag eltávolít egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="1aaf2-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1aaf2-114">-ApplicationName</span></span>
<span data-ttu-id="1aaf2-115">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="1aaf2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aaf2-116">-DefaultProfile</span></span>
<span data-ttu-id="1aaf2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aaf2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aaf2-118">-ResourceGroupName</span></span>
<span data-ttu-id="1aaf2-119">A Batch-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="1aaf2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaf2-120">CommonParameters</span></span>
<span data-ttu-id="1aaf2-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aaf2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaf2-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aaf2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaf2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1aaf2-123">INPUTS</span></span>

### <span data-ttu-id="1aaf2-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1aaf2-124">System.String</span></span>

## <span data-ttu-id="1aaf2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aaf2-125">OUTPUTS</span></span>

### <span data-ttu-id="1aaf2-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="1aaf2-126">System.Void</span></span>

## <span data-ttu-id="1aaf2-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1aaf2-127">NOTES</span></span>

## <span data-ttu-id="1aaf2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1aaf2-128">RELATED LINKS</span></span>

[<span data-ttu-id="1aaf2-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1aaf2-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="1aaf2-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1aaf2-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="1aaf2-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1aaf2-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="1aaf2-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1aaf2-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="1aaf2-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1aaf2-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="1aaf2-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1aaf2-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


