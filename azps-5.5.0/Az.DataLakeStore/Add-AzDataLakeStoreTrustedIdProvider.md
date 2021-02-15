---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161922"
---
# <span data-ttu-id="d3e6c-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d3e6c-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d3e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e6c-103">Hozzáad egy megbízható identitásszolgáltatót a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d3e6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3e6c-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3e6c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e6c-106">Az **Add-AzDataLakeStoreTrustedIdProvider** parancsmag hozzáad egy megbízható identitásszolgáltatót a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d3e6c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e6c-108">1. példa: Megbízható identitásszolgáltató hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d3e6c-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="d3e6c-109">Felveszi a "MyProvider" szolgáltatót a "ContosoADL" fiókba a "szolgáltató végpontjával" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 " "</span><span class="sxs-lookup"><span data-stu-id="d3e6c-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="d3e6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="d3e6c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d3e6c-111">-Account</span></span>
<span data-ttu-id="d3e6c-112">Annak a Data Lake Store-fióknak a neve, amelybe fel kell venni a megadott megbízható identitásszolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="d3e6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e6c-113">-DefaultProfile</span></span>
<span data-ttu-id="d3e6c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d3e6c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3e6c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d3e6c-115">-Name</span></span>
<span data-ttu-id="d3e6c-116">A hozzáadható megbízható identitásszolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="d3e6c-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="d3e6c-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3e6c-117">-ProviderEndpoint</span></span>
<span data-ttu-id="d3e6c-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="d3e6c-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="d3e6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3e6c-120">Annak az erőforráscsoportnak a neve, amely alatt a megbízható identitásszolgáltatót hozzáadható fiók tartozik.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="d3e6c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e6c-121">-Confirm</span></span>
<span data-ttu-id="d3e6c-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e6c-123">-WhatIf</span></span>
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

### <span data-ttu-id="d3e6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e6c-124">CommonParameters</span></span>
<span data-ttu-id="d3e6c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e6c-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e6c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e6c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3e6c-127">INPUTS</span></span>

### <span data-ttu-id="d3e6c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e6c-128">System.String</span></span>

## <span data-ttu-id="d3e6c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3e6c-129">OUTPUTS</span></span>

### <span data-ttu-id="d3e6c-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d3e6c-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d3e6c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3e6c-131">NOTES</span></span>

## <span data-ttu-id="d3e6c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3e6c-132">RELATED LINKS</span></span>
