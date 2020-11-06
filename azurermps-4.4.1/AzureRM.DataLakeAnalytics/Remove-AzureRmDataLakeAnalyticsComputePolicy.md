---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501912"
---
# <span data-ttu-id="12621-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="12621-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="12621-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12621-102">SYNOPSIS</span></span>
<span data-ttu-id="12621-103">A megadott Azure Data Lake Analytics számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="12621-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12621-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12621-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12621-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12621-105">DESCRIPTION</span></span>
<span data-ttu-id="12621-106">A **Remove-AzureRmDataLakeAnalyticsComputePolicy** eltávolítja a megadott Azure Data Lake Analytics számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="12621-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="12621-107">Példák</span><span class="sxs-lookup"><span data-stu-id="12621-107">EXAMPLES</span></span>

### <span data-ttu-id="12621-108">1. példa: számítási házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="12621-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="12621-109">Ez a parancs eltávolítja a megadott számítási házirendet a "myPolicy" névvel a "contosoadla" fiókban.</span><span class="sxs-lookup"><span data-stu-id="12621-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="12621-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12621-110">PARAMETERS</span></span>

### <span data-ttu-id="12621-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="12621-111">-Account</span></span>
<span data-ttu-id="12621-112">Annak a fióknak a neve, amelyből el szeretné távolítani a számítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="12621-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="12621-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12621-113">-Name</span></span>
<span data-ttu-id="12621-114">Az eltávolítandó számítási szabály neve.</span><span class="sxs-lookup"><span data-stu-id="12621-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="12621-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12621-115">-PassThru</span></span>
<span data-ttu-id="12621-116">Sikeres törlés esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="12621-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="12621-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12621-117">-ResourceGroupName</span></span>
<span data-ttu-id="12621-118">Annak az erőforráscsoport-csoportnak a neve, amelyben a fiók létezik.</span><span class="sxs-lookup"><span data-stu-id="12621-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="12621-119">Nem kötelező, és a program megkísérli kideríteni, hogy nincs-e megadva.</span><span class="sxs-lookup"><span data-stu-id="12621-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="12621-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12621-120">-Confirm</span></span>
<span data-ttu-id="12621-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12621-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12621-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12621-122">-WhatIf</span></span>
<span data-ttu-id="12621-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12621-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12621-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12621-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12621-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12621-125">-DefaultProfile</span></span>
<span data-ttu-id="12621-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12621-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12621-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12621-127">CommonParameters</span></span>
<span data-ttu-id="12621-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12621-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12621-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12621-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12621-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12621-130">INPUTS</span></span>

### <span data-ttu-id="12621-131">System. String</span><span class="sxs-lookup"><span data-stu-id="12621-131">System.String</span></span>

## <span data-ttu-id="12621-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12621-132">OUTPUTS</span></span>

### <span data-ttu-id="12621-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12621-133">System.Boolean</span></span>

## <span data-ttu-id="12621-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12621-134">NOTES</span></span>

## <span data-ttu-id="12621-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12621-135">RELATED LINKS</span></span>

