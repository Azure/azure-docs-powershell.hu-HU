---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494073"
---
# <span data-ttu-id="af980-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="af980-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="af980-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af980-102">SYNOPSIS</span></span>
<span data-ttu-id="af980-103">A megadott Azure Data Lake Analytics számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af980-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af980-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af980-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af980-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af980-105">DESCRIPTION</span></span>
<span data-ttu-id="af980-106">A **Remove-AzureRmDataLakeAnalyticsComputePolicy** eltávolítja a megadott Azure Data Lake Analytics számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="af980-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="af980-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af980-107">EXAMPLES</span></span>

### <span data-ttu-id="af980-108">1. példa: számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af980-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="af980-109">Ez a parancs eltávolítja a megadott számítási házirendet a "myPolicy" névvel a "contosoadla" fiókban.</span><span class="sxs-lookup"><span data-stu-id="af980-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="af980-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af980-110">PARAMETERS</span></span>

### <span data-ttu-id="af980-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="af980-111">-Account</span></span>
<span data-ttu-id="af980-112">Annak a fióknak a neve, amelyből el szeretné távolítani a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="af980-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="af980-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af980-113">-DefaultProfile</span></span>
<span data-ttu-id="af980-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af980-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af980-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af980-115">-Name</span></span>
<span data-ttu-id="af980-116">Az eltávolítandó számítási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="af980-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="af980-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af980-117">-PassThru</span></span>
<span data-ttu-id="af980-118">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="af980-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="af980-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af980-119">-ResourceGroupName</span></span>
<span data-ttu-id="af980-120">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="af980-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="af980-121">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="af980-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="af980-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af980-122">-Confirm</span></span>
<span data-ttu-id="af980-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af980-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af980-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af980-124">-WhatIf</span></span>
<span data-ttu-id="af980-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af980-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af980-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af980-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af980-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af980-127">CommonParameters</span></span>
<span data-ttu-id="af980-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af980-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af980-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af980-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af980-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af980-130">INPUTS</span></span>

### <span data-ttu-id="af980-131">System. String</span><span class="sxs-lookup"><span data-stu-id="af980-131">System.String</span></span>

## <span data-ttu-id="af980-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af980-132">OUTPUTS</span></span>

### <span data-ttu-id="af980-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af980-133">System.Boolean</span></span>

## <span data-ttu-id="af980-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af980-134">NOTES</span></span>

## <span data-ttu-id="af980-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af980-135">RELATED LINKS</span></span>
