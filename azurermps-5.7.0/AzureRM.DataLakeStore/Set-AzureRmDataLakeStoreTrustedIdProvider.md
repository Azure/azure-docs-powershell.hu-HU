---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 29f9bbab5d3f7590d53bc405d80ea9e5c484fd5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497647"
---
# <span data-ttu-id="1d369-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1d369-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1d369-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d369-102">SYNOPSIS</span></span>
<span data-ttu-id="1d369-103">Módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="1d369-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d369-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d369-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d369-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d369-105">DESCRIPTION</span></span>
<span data-ttu-id="1d369-106">A **set-AzureRmDataLakeStoreTrustedIdProvider** parancsmag módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="1d369-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1d369-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d369-107">EXAMPLES</span></span>

### <span data-ttu-id="1d369-108">Példa 1: a megbízható identitás-szolgáltató végpontjának frissítése</span><span class="sxs-lookup"><span data-stu-id="1d369-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="1d369-109">Ezzel frissíti a szolgáltatói endpoing a "MyProvider" ContosoADL "" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="1d369-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="1d369-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d369-110">PARAMETERS</span></span>

### <span data-ttu-id="1d369-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="1d369-111">-Account</span></span>
<span data-ttu-id="1d369-112">Az adattó-tároló fiók a megbízható identitás-Szolgáltató hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="1d369-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d369-113">-DefaultProfile</span></span>
<span data-ttu-id="1d369-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d369-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d369-115">-Name</span></span>
<span data-ttu-id="1d369-116">A megbízható identitás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="1d369-116">The name of the trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d369-117">-ProviderEndpoint</span></span>
<span data-ttu-id="1d369-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="1d369-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d369-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d369-120">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazó erőforráscsoportot frissíti a megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="1d369-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d369-121">-Confirm</span></span>
<span data-ttu-id="1d369-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d369-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d369-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d369-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d369-124">CommonParameters</span></span>
<span data-ttu-id="1d369-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d369-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d369-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d369-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d369-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d369-127">INPUTS</span></span>

### <span data-ttu-id="1d369-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="1d369-128">None</span></span>
<span data-ttu-id="1d369-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1d369-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d369-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d369-130">OUTPUTS</span></span>

### <span data-ttu-id="1d369-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1d369-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="1d369-132">A frissített megbízható identitás-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="1d369-132">The updated trusted identity provider.</span></span>

## <span data-ttu-id="1d369-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d369-133">NOTES</span></span>

## <span data-ttu-id="1d369-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d369-134">RELATED LINKS</span></span>

