---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: cf35c2817e32045e3e0a9e236f1c92f7f273407c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836253"
---
# <span data-ttu-id="cdfba-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="cdfba-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="cdfba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdfba-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfba-103">Módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="cdfba-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cdfba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdfba-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdfba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdfba-105">DESCRIPTION</span></span>
<span data-ttu-id="cdfba-106">A **set-AzDataLakeStoreTrustedIdProvider** parancsmag módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="cdfba-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cdfba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cdfba-107">EXAMPLES</span></span>

### <span data-ttu-id="cdfba-108">Példa 1: a megbízható identitás-szolgáltató végpontjának frissítése</span><span class="sxs-lookup"><span data-stu-id="cdfba-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="cdfba-109">Ezzel frissíti a szolgáltatói endpoing a "MyProvider" ContosoADL "" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="cdfba-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="cdfba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdfba-110">PARAMETERS</span></span>

### <span data-ttu-id="cdfba-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="cdfba-111">-Account</span></span>
<span data-ttu-id="cdfba-112">Az adattó-tároló fiók a megbízható identitás-Szolgáltató hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="cdfba-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="cdfba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfba-113">-DefaultProfile</span></span>
<span data-ttu-id="cdfba-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cdfba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdfba-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdfba-115">-Name</span></span>
<span data-ttu-id="cdfba-116">A megbízható identitás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="cdfba-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="cdfba-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="cdfba-117">-ProviderEndpoint</span></span>
<span data-ttu-id="cdfba-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/\<provider identitás\></span><span class="sxs-lookup"><span data-stu-id="cdfba-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfba-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdfba-120">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazó erőforráscsoportot frissíti a megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="cdfba-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfba-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdfba-121">-Confirm</span></span>
<span data-ttu-id="cdfba-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdfba-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfba-123">-WhatIf</span></span>
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

### <span data-ttu-id="cdfba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfba-124">CommonParameters</span></span>
<span data-ttu-id="cdfba-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdfba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfba-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfba-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdfba-127">INPUTS</span></span>

### <span data-ttu-id="cdfba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cdfba-128">System.String</span></span>

## <span data-ttu-id="cdfba-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdfba-129">OUTPUTS</span></span>

### <span data-ttu-id="cdfba-130">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="cdfba-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="cdfba-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdfba-131">NOTES</span></span>

## <span data-ttu-id="cdfba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdfba-132">RELATED LINKS</span></span>
