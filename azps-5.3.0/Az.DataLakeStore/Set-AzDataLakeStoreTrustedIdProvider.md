---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465783"
---
# <span data-ttu-id="0f8a7-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0f8a7-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0f8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8a7-103">Módosítja a megadott megbízható identitásszolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0f8a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f8a7-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f8a7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f8a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0f8a7-106">A **Set-AzDataLakeStoreTrustedIdProvider** parancsmag módosítja a megadott megbízható identitásszolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0f8a7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f8a7-107">EXAMPLES</span></span>

### <span data-ttu-id="0f8a7-108">1. példa: Megbízható identitásszolgáltató végpontjának frissítése</span><span class="sxs-lookup"><span data-stu-id="0f8a7-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="0f8a7-109">Ez a "ContosoADL" fiók "MyProvider" tűzfalszabályának szolgáltatói végpontját a következőre https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 frissíti: "</span><span class="sxs-lookup"><span data-stu-id="0f8a7-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="0f8a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f8a7-110">PARAMETERS</span></span>

### <span data-ttu-id="0f8a7-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0f8a7-111">-Account</span></span>
<span data-ttu-id="0f8a7-112">The Data Lake Store account to add the trusted identity provider to</span><span class="sxs-lookup"><span data-stu-id="0f8a7-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="0f8a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8a7-113">-DefaultProfile</span></span>
<span data-ttu-id="0f8a7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f8a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f8a7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f8a7-115">-Name</span></span>
<span data-ttu-id="0f8a7-116">A megbízható identitásszolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="0f8a7-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f8a7-117">-ProviderEndpoint</span></span>
<span data-ttu-id="0f8a7-118">Az érvényes megbízható szolgáltató végpontja a következő formátumban: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="0f8a7-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="0f8a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f8a7-120">Annak az erőforráscsoportnak a neve, amely a megbízható identitásszolgáltató frissítéséhez szükséges fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="0f8a7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f8a7-121">-Confirm</span></span>
<span data-ttu-id="0f8a7-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8a7-123">-WhatIf</span></span>
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

### <span data-ttu-id="0f8a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8a7-124">CommonParameters</span></span>
<span data-ttu-id="0f8a7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8a7-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8a7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8a7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f8a7-127">INPUTS</span></span>

### <span data-ttu-id="0f8a7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0f8a7-128">System.String</span></span>

## <span data-ttu-id="0f8a7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f8a7-129">OUTPUTS</span></span>

### <span data-ttu-id="0f8a7-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0f8a7-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0f8a7-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f8a7-131">NOTES</span></span>

## <span data-ttu-id="0f8a7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f8a7-132">RELATED LINKS</span></span>
