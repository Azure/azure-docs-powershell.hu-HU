---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 12e84ee5456acc0c56eed0f35b0bf3c23813b31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493515"
---
# <span data-ttu-id="38b59-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="38b59-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="38b59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38b59-102">SYNOPSIS</span></span>
<span data-ttu-id="38b59-103">Módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="38b59-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38b59-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38b59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38b59-105">DESCRIPTION</span></span>
<span data-ttu-id="38b59-106">A **set-AzureRmDataLakeStoreTrustedIdProvider** parancsmag módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="38b59-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="38b59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38b59-107">EXAMPLES</span></span>

### <span data-ttu-id="38b59-108">Példa 1: a megbízható identitás-szolgáltató végpontjának frissítése</span><span class="sxs-lookup"><span data-stu-id="38b59-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="38b59-109">Ezzel frissíti a szolgáltatói endpoing a "MyProvider" ContosoADL "" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="38b59-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="38b59-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38b59-110">PARAMETERS</span></span>

### <span data-ttu-id="38b59-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="38b59-111">-Account</span></span>
<span data-ttu-id="38b59-112">Az adattó-tároló fiók a megbízható identitás-Szolgáltató hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="38b59-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="38b59-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38b59-113">-Name</span></span>
<span data-ttu-id="38b59-114">A megbízható identitás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="38b59-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="38b59-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="38b59-115">-ProviderEndpoint</span></span>
<span data-ttu-id="38b59-116">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="38b59-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="38b59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b59-117">-ResourceGroupName</span></span>
<span data-ttu-id="38b59-118">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazó erőforráscsoportot frissíti a megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="38b59-118">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="38b59-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38b59-119">-Confirm</span></span>
<span data-ttu-id="38b59-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38b59-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b59-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b59-121">-WhatIf</span></span>
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

### <span data-ttu-id="38b59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b59-122">-DefaultProfile</span></span>
<span data-ttu-id="38b59-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38b59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38b59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b59-124">CommonParameters</span></span>
<span data-ttu-id="38b59-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38b59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b59-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b59-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b59-127">INPUTS</span></span>

## <span data-ttu-id="38b59-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b59-128">OUTPUTS</span></span>

### <span data-ttu-id="38b59-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="38b59-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="38b59-130">A frissített megbízható identitás-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="38b59-130">The updated trusted identity provider.</span></span>

## <span data-ttu-id="38b59-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38b59-131">NOTES</span></span>

## <span data-ttu-id="38b59-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38b59-132">RELATED LINKS</span></span>

