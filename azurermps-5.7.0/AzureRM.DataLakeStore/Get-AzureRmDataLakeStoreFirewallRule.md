---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494519"
---
# <span data-ttu-id="fd4b2-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd4b2-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="fd4b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4b2-103">A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="fd4b2-104">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd4b2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd4b2-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4b2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd4b2-106">DESCRIPTION</span></span>
<span data-ttu-id="fd4b2-107">A Get-AzureRmDataLakeStoreFirewallRule parancsmag a megadott adattó-tárolóban kapja meg a megadott tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="fd4b2-108">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="fd4b2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fd4b2-109">EXAMPLES</span></span>

### <span data-ttu-id="fd4b2-110">Példa 1: adott tűzfalszabály beolvasása</span><span class="sxs-lookup"><span data-stu-id="fd4b2-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="fd4b2-111">A "MyFirewallRule" nevű tűzfal-szabályt számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="fd4b2-112">2. példa: az összes tűzfal-szabály listázása egy fiókban</span><span class="sxs-lookup"><span data-stu-id="fd4b2-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="fd4b2-113">A "ContosoADL" fiók minden tűzfal-szabályát visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="fd4b2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd4b2-114">PARAMETERS</span></span>

### <span data-ttu-id="fd4b2-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fd4b2-115">-Account</span></span>
<span data-ttu-id="fd4b2-116">Az adattó-tároló fiókja a tűzfalszabály beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="fd4b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4b2-117">-DefaultProfile</span></span>
<span data-ttu-id="fd4b2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd4b2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd4b2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd4b2-119">-Name</span></span>
<span data-ttu-id="fd4b2-120">A lekérdezni kívánt tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="fd4b2-120">The name of the firewall rule to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd4b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd4b2-122">Annak az erőforráscsoport-csoportnak a neve, amely alatt le szeretné olvasni a megadott fiók megadott tűzfalszabályét.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4b2-123">CommonParameters</span></span>
<span data-ttu-id="fd4b2-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd4b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4b2-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd4b2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4b2-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd4b2-126">INPUTS</span></span>

### <span data-ttu-id="fd4b2-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="fd4b2-127">None</span></span>
<span data-ttu-id="fd4b2-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd4b2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd4b2-129">OUTPUTS</span></span>

### <span data-ttu-id="fd4b2-130">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd4b2-130">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="fd4b2-131">A lekérdezni kívánt tűzfal-szabály</span><span class="sxs-lookup"><span data-stu-id="fd4b2-131">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="fd4b2-132">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="fd4b2-132">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="fd4b2-133">A megadott fiók tűzfal-szabályainak listája.</span><span class="sxs-lookup"><span data-stu-id="fd4b2-133">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="fd4b2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd4b2-134">NOTES</span></span>

## <span data-ttu-id="fd4b2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd4b2-135">RELATED LINKS</span></span>

