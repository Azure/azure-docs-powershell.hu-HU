---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165362"
---
# <span data-ttu-id="b0758-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0758-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b0758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0758-102">SYNOPSIS</span></span>
<span data-ttu-id="b0758-103">Lekérte a megadott megbízható identitásszolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="b0758-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="b0758-104">Ha nincs megadva szolgáltató, akkor felsorolja a fiók összes szolgáltatóját.</span><span class="sxs-lookup"><span data-stu-id="b0758-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="b0758-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0758-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0758-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0758-106">DESCRIPTION</span></span>
<span data-ttu-id="b0758-107">A **Get-AzDataLakeStoreTrustedIdProvider** parancsmag megkapja a megadott megbízható identitásszolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="b0758-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="b0758-108">Ha nincs megadva szolgáltató, akkor felsorolja a fiók összes szolgáltatóját.</span><span class="sxs-lookup"><span data-stu-id="b0758-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="b0758-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0758-109">EXAMPLES</span></span>

### <span data-ttu-id="b0758-110">1. példa: Adott megbízható identitásszolgáltató lekérte</span><span class="sxs-lookup"><span data-stu-id="b0758-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="b0758-111">A "ContosoADL" fiókból a "MyProvider" nevű szolgáltatót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b0758-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="b0758-112">2. példa: Egy fiók összes szolgáltatóának felsorolása</span><span class="sxs-lookup"><span data-stu-id="b0758-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="b0758-113">A "ContosoADL" fiókban található összes szolgáltató listája</span><span class="sxs-lookup"><span data-stu-id="b0758-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="b0758-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0758-114">PARAMETERS</span></span>

### <span data-ttu-id="b0758-115">-Account</span><span class="sxs-lookup"><span data-stu-id="b0758-115">-Account</span></span>
<span data-ttu-id="b0758-116">The Data Lake Store account to retrieve the trusted identity provider from</span><span class="sxs-lookup"><span data-stu-id="b0758-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="b0758-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0758-117">-DefaultProfile</span></span>
<span data-ttu-id="b0758-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0758-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0758-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b0758-119">-Name</span></span>
<span data-ttu-id="b0758-120">A lekért megbízható identitásszolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="b0758-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0758-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0758-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0758-122">Annak az erőforráscsoportnak a neve, amely alatt le szeretnékérni a megadott fiók megadott megbízható identitásszolgáltatóját.</span><span class="sxs-lookup"><span data-stu-id="b0758-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0758-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0758-123">CommonParameters</span></span>
<span data-ttu-id="b0758-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0758-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0758-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0758-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0758-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0758-126">INPUTS</span></span>

### <span data-ttu-id="b0758-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b0758-127">System.String</span></span>

## <span data-ttu-id="b0758-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0758-128">OUTPUTS</span></span>

### <span data-ttu-id="b0758-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0758-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="b0758-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0758-130">NOTES</span></span>

## <span data-ttu-id="b0758-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0758-131">RELATED LINKS</span></span>
