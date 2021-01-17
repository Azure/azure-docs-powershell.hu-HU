---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465863"
---
# <span data-ttu-id="a3ff2-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="a3ff2-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="a3ff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ff2-103">Egy megadott Azure Data Lake Analytics számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3ff2-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="a3ff2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3ff2-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ff2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ff2-106">A **Remove-AzDataLakeAnalyticsComputePolicy** eltávolít egy megadott Azure Data Lake Analytics számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="a3ff2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3ff2-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ff2-108">1. példa: Számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3ff2-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="a3ff2-109">Ez a parancs eltávolítja a "contosoadla" fiókban a "myPolicy" nevű megadott számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="a3ff2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ff2-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ff2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a3ff2-111">-Account</span></span>
<span data-ttu-id="a3ff2-112">Annak a fióknak a neve, amelyből el szeretné távolítani a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="a3ff2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ff2-113">-DefaultProfile</span></span>
<span data-ttu-id="a3ff2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3ff2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3ff2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a3ff2-115">-Name</span></span>
<span data-ttu-id="a3ff2-116">Az eltávolítható számítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="a3ff2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3ff2-117">-PassThru</span></span>
<span data-ttu-id="a3ff2-118">Sikeres törléskor a return true (igaz) érték.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="a3ff2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ff2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3ff2-120">Annak az erőforráscsoportnak a neve, amely alatt a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="a3ff2-121">Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="a3ff2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3ff2-122">-Confirm</span></span>
<span data-ttu-id="a3ff2-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ff2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ff2-124">-WhatIf</span></span>
<span data-ttu-id="a3ff2-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ff2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ff2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ff2-127">CommonParameters</span></span>
<span data-ttu-id="a3ff2-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ff2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ff2-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ff2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ff2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3ff2-130">INPUTS</span></span>

### <span data-ttu-id="a3ff2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a3ff2-131">System.String</span></span>

## <span data-ttu-id="a3ff2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ff2-132">OUTPUTS</span></span>

### <span data-ttu-id="a3ff2-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3ff2-133">System.Boolean</span></span>

## <span data-ttu-id="a3ff2-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3ff2-134">NOTES</span></span>

## <span data-ttu-id="a3ff2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3ff2-135">RELATED LINKS</span></span>
