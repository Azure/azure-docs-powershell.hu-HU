---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298040"
---
# <span data-ttu-id="3fdc2-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3fdc2-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3fdc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3fdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdc2-103">A megadott Azure Data Lake Analytics számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3fdc2-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="3fdc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3fdc2-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3fdc2-105">DESCRIPTION</span></span>
<span data-ttu-id="3fdc2-106">A **Remove-AzDataLakeAnalyticsComputePolicy** eltávolítja a megadott Azure Data Lake Analytics számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="3fdc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3fdc2-107">EXAMPLES</span></span>

### <span data-ttu-id="3fdc2-108">1. példa: számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3fdc2-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="3fdc2-109">Ez a parancs eltávolítja a megadott számítási házirendet a "myPolicy" névvel a "contosoadla" fiókban.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="3fdc2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3fdc2-110">PARAMETERS</span></span>

### <span data-ttu-id="3fdc2-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="3fdc2-111">-Account</span></span>
<span data-ttu-id="3fdc2-112">Annak a fióknak a neve, amelyből el szeretné távolítani a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="3fdc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdc2-113">-DefaultProfile</span></span>
<span data-ttu-id="3fdc2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3fdc2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fdc2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3fdc2-115">-Name</span></span>
<span data-ttu-id="3fdc2-116">Az eltávolítandó számítási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="3fdc2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fdc2-117">-PassThru</span></span>
<span data-ttu-id="3fdc2-118">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="3fdc2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdc2-119">-ResourceGroupName</span></span>
<span data-ttu-id="3fdc2-120">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3fdc2-121">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3fdc2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3fdc2-122">-Confirm</span></span>
<span data-ttu-id="3fdc2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdc2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdc2-124">-WhatIf</span></span>
<span data-ttu-id="3fdc2-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdc2-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fdc2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdc2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdc2-127">CommonParameters</span></span>
<span data-ttu-id="3fdc2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3fdc2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdc2-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdc2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdc2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fdc2-130">INPUTS</span></span>

### <span data-ttu-id="3fdc2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3fdc2-131">System.String</span></span>

## <span data-ttu-id="3fdc2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fdc2-132">OUTPUTS</span></span>

### <span data-ttu-id="3fdc2-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fdc2-133">System.Boolean</span></span>

## <span data-ttu-id="3fdc2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3fdc2-134">NOTES</span></span>

## <span data-ttu-id="3fdc2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fdc2-135">RELATED LINKS</span></span>
