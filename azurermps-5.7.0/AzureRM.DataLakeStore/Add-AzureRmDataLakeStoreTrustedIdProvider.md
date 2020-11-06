---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 302ad6ac14ad9fcb08053e70afb7951e72c6e027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496599"
---
# <span data-ttu-id="f628d-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f628d-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f628d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f628d-102">SYNOPSIS</span></span>
<span data-ttu-id="f628d-103">A megadott Data Lake Store-fiókhoz hozzáadja a megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="f628d-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f628d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f628d-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f628d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f628d-105">DESCRIPTION</span></span>
<span data-ttu-id="f628d-106">Az **Add-AzureRmDataLakeStoreTrustedIdProvider** parancsmag egy megbízható identitás-szolgáltatót ad hozzá a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f628d-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f628d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f628d-107">EXAMPLES</span></span>

### <span data-ttu-id="f628d-108">1. példa: megbízható identitás-szolgáltató hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f628d-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="f628d-109">A "MyProvider" szolgáltató felveszi a "ContosoADL" fiókot a szolgáltató végpontjának " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="f628d-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="f628d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f628d-110">PARAMETERS</span></span>

### <span data-ttu-id="f628d-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="f628d-111">-Account</span></span>
<span data-ttu-id="f628d-112">Az adattó-tároló fiók neve, amely a megadott megbízható identitás-szolgáltatót adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="f628d-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="f628d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f628d-113">-DefaultProfile</span></span>
<span data-ttu-id="f628d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f628d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f628d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f628d-115">-Name</span></span>
<span data-ttu-id="f628d-116">A felvenni kívánt megbízható személyazonosság-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="f628d-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="f628d-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="f628d-117">-ProviderEndpoint</span></span>
<span data-ttu-id="f628d-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="f628d-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="f628d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f628d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f628d-120">Annak az erőforráscsoportnek a neve, amely alatt a megbízható személyazonosság-szolgáltatót felvenni kívánt fiók.</span><span class="sxs-lookup"><span data-stu-id="f628d-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="f628d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f628d-121">-Confirm</span></span>
<span data-ttu-id="f628d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f628d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f628d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f628d-123">-WhatIf</span></span>
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

### <span data-ttu-id="f628d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f628d-124">CommonParameters</span></span>
<span data-ttu-id="f628d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f628d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f628d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f628d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f628d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f628d-127">INPUTS</span></span>

### <span data-ttu-id="f628d-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="f628d-128">None</span></span>
<span data-ttu-id="f628d-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f628d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f628d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f628d-130">OUTPUTS</span></span>

### <span data-ttu-id="f628d-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f628d-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="f628d-132">A felvett megbízható identitás szolgáltatója.</span><span class="sxs-lookup"><span data-stu-id="f628d-132">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="f628d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f628d-133">NOTES</span></span>

## <span data-ttu-id="f628d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f628d-134">RELATED LINKS</span></span>

