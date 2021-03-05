---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004261"
---
# <span data-ttu-id="7caa3-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7caa3-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="7caa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7caa3-102">SYNOPSIS</span></span>
<span data-ttu-id="7caa3-103">Egy Data Lake Analytics-fiók törlése.</span><span class="sxs-lookup"><span data-stu-id="7caa3-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7caa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7caa3-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7caa3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7caa3-105">DESCRIPTION</span></span>
<span data-ttu-id="7caa3-106">A **Remove-AzDataLakeAnalyticsAccount** parancsmag véglegesen töröl egy Azure Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="7caa3-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7caa3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7caa3-107">EXAMPLES</span></span>

### <span data-ttu-id="7caa3-108">1. példa: Fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7caa3-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="7caa3-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="7caa3-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="7caa3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7caa3-110">PARAMETERS</span></span>

### <span data-ttu-id="7caa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7caa3-111">-DefaultProfile</span></span>
<span data-ttu-id="7caa3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7caa3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7caa3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7caa3-113">-Force</span></span>
<span data-ttu-id="7caa3-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7caa3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7caa3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7caa3-115">-Name</span></span>
<span data-ttu-id="7caa3-116">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7caa3-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7caa3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7caa3-117">-PassThru</span></span>
<span data-ttu-id="7caa3-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="7caa3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7caa3-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7caa3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7caa3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7caa3-120">-ResourceGroupName</span></span>
<span data-ttu-id="7caa3-121">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7caa3-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="7caa3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7caa3-122">-Confirm</span></span>
<span data-ttu-id="7caa3-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7caa3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7caa3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7caa3-124">-WhatIf</span></span>
<span data-ttu-id="7caa3-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7caa3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7caa3-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7caa3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7caa3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7caa3-127">CommonParameters</span></span>
<span data-ttu-id="7caa3-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7caa3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7caa3-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7caa3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7caa3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7caa3-130">INPUTS</span></span>

### <span data-ttu-id="7caa3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7caa3-131">System.String</span></span>

## <span data-ttu-id="7caa3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7caa3-132">OUTPUTS</span></span>

### <span data-ttu-id="7caa3-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7caa3-133">System.Boolean</span></span>

## <span data-ttu-id="7caa3-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7caa3-134">NOTES</span></span>

## <span data-ttu-id="7caa3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7caa3-135">RELATED LINKS</span></span>

[<span data-ttu-id="7caa3-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7caa3-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7caa3-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7caa3-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7caa3-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7caa3-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7caa3-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7caa3-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


