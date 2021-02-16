---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204382"
---
# <span data-ttu-id="b9d82-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9d82-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b9d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9d82-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d82-103">Egy Data Lake Analytics-fiók törlése.</span><span class="sxs-lookup"><span data-stu-id="b9d82-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="b9d82-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9d82-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9d82-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9d82-105">DESCRIPTION</span></span>
<span data-ttu-id="b9d82-106">A **Remove-AzDataLakeAnalyticsAccount** parancsmag véglegesen töröl egy Azure Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b9d82-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b9d82-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9d82-107">EXAMPLES</span></span>

### <span data-ttu-id="b9d82-108">1. példa: Fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b9d82-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="b9d82-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b9d82-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="b9d82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9d82-110">PARAMETERS</span></span>

### <span data-ttu-id="b9d82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d82-111">-DefaultProfile</span></span>
<span data-ttu-id="b9d82-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9d82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9d82-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b9d82-113">-Force</span></span>
<span data-ttu-id="b9d82-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b9d82-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d82-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b9d82-115">-Name</span></span>
<span data-ttu-id="b9d82-116">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d82-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b9d82-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9d82-117">-PassThru</span></span>
<span data-ttu-id="b9d82-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="b9d82-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9d82-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b9d82-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9d82-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9d82-121">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9d82-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d82-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9d82-122">-Confirm</span></span>
<span data-ttu-id="b9d82-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9d82-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d82-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9d82-124">-WhatIf</span></span>
<span data-ttu-id="b9d82-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9d82-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9d82-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9d82-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d82-127">CommonParameters</span></span>
<span data-ttu-id="b9d82-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9d82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d82-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9d82-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d82-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9d82-130">INPUTS</span></span>

### <span data-ttu-id="b9d82-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9d82-131">System.String</span></span>

## <span data-ttu-id="b9d82-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9d82-132">OUTPUTS</span></span>

### <span data-ttu-id="b9d82-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9d82-133">System.Boolean</span></span>

## <span data-ttu-id="b9d82-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9d82-134">NOTES</span></span>

## <span data-ttu-id="b9d82-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9d82-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9d82-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9d82-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b9d82-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9d82-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b9d82-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9d82-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b9d82-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9d82-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


