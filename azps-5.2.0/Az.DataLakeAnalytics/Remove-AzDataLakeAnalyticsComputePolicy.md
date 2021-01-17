---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372859"
---
# <span data-ttu-id="d4193-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d4193-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d4193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4193-102">SYNOPSIS</span></span>
<span data-ttu-id="d4193-103">Egy megadott Azure Data Lake Analytics számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4193-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="d4193-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4193-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4193-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4193-105">DESCRIPTION</span></span>
<span data-ttu-id="d4193-106">A **Remove-AzDataLakeAnalyticsComputePolicy** eltávolít egy megadott Azure Data Lake Analytics számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="d4193-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="d4193-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4193-107">EXAMPLES</span></span>

### <span data-ttu-id="d4193-108">1. példa: Számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4193-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="d4193-109">Ez a parancs eltávolítja a "contosoadla" fiókban a "myPolicy" nevű megadott számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="d4193-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="d4193-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4193-110">PARAMETERS</span></span>

### <span data-ttu-id="d4193-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d4193-111">-Account</span></span>
<span data-ttu-id="d4193-112">Annak a fióknak a neve, amelyből el szeretné távolítani a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="d4193-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4193-113">-DefaultProfile</span></span>
<span data-ttu-id="d4193-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4193-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4193-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d4193-115">-Name</span></span>
<span data-ttu-id="d4193-116">Az eltávolítható számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="d4193-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4193-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4193-117">-PassThru</span></span>
<span data-ttu-id="d4193-118">Sikeres törléskor a return true (igaz) érték.</span><span class="sxs-lookup"><span data-stu-id="d4193-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4193-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4193-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4193-120">Annak az erőforráscsoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="d4193-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="d4193-121">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="d4193-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4193-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4193-122">-Confirm</span></span>
<span data-ttu-id="d4193-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4193-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4193-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4193-124">-WhatIf</span></span>
<span data-ttu-id="d4193-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4193-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4193-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4193-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4193-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4193-127">CommonParameters</span></span>
<span data-ttu-id="d4193-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4193-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4193-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4193-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4193-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4193-130">INPUTS</span></span>

### <span data-ttu-id="d4193-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4193-131">System.String</span></span>

## <span data-ttu-id="d4193-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4193-132">OUTPUTS</span></span>

### <span data-ttu-id="d4193-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4193-133">System.Boolean</span></span>

## <span data-ttu-id="d4193-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4193-134">NOTES</span></span>

## <span data-ttu-id="d4193-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4193-135">RELATED LINKS</span></span>
