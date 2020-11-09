---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297938"
---
# <span data-ttu-id="9981e-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="9981e-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="9981e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9981e-102">SYNOPSIS</span></span>
<span data-ttu-id="9981e-103">A megadott Data Lake Store-fiókhoz hozzáadja a megbízható identitás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="9981e-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9981e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9981e-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9981e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9981e-105">DESCRIPTION</span></span>
<span data-ttu-id="9981e-106">Az **Add-AzDataLakeStoreTrustedIdProvider** parancsmag egy megbízható identitás-szolgáltatót ad hozzá a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="9981e-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9981e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9981e-107">EXAMPLES</span></span>

### <span data-ttu-id="9981e-108">1. példa: megbízható identitás-szolgáltató hozzáadása</span><span class="sxs-lookup"><span data-stu-id="9981e-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="9981e-109">A "MyProvider" szolgáltató felveszi a "ContosoADL" fiókot a szolgáltató végpontjának " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="9981e-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="9981e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9981e-110">PARAMETERS</span></span>

### <span data-ttu-id="9981e-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9981e-111">-Account</span></span>
<span data-ttu-id="9981e-112">Az adattó-tároló fiók neve, amely a megadott megbízható identitás-szolgáltatót adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="9981e-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="9981e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9981e-113">-DefaultProfile</span></span>
<span data-ttu-id="9981e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9981e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9981e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9981e-115">-Name</span></span>
<span data-ttu-id="9981e-116">A felvenni kívánt megbízható személyazonosság-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="9981e-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="9981e-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="9981e-117">-ProviderEndpoint</span></span>
<span data-ttu-id="9981e-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="9981e-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="9981e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9981e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9981e-120">Annak az erőforráscsoportnek a neve, amely alatt a megbízható személyazonosság-szolgáltatót felvenni kívánt fiók.</span><span class="sxs-lookup"><span data-stu-id="9981e-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="9981e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9981e-121">-Confirm</span></span>
<span data-ttu-id="9981e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9981e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9981e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9981e-123">-WhatIf</span></span>
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

### <span data-ttu-id="9981e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9981e-124">CommonParameters</span></span>
<span data-ttu-id="9981e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9981e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9981e-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9981e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9981e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9981e-127">INPUTS</span></span>

### <span data-ttu-id="9981e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9981e-128">System.String</span></span>

## <span data-ttu-id="9981e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9981e-129">OUTPUTS</span></span>

### <span data-ttu-id="9981e-130">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="9981e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="9981e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9981e-131">NOTES</span></span>

## <span data-ttu-id="9981e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9981e-132">RELATED LINKS</span></span>
