---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679466"
---
# <span data-ttu-id="56aea-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="56aea-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="56aea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56aea-102">SYNOPSIS</span></span>
<span data-ttu-id="56aea-103">A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="56aea-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="56aea-104">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="56aea-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56aea-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56aea-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56aea-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="56aea-106">DESCRIPTION</span></span>
<span data-ttu-id="56aea-107">A Get-AzureRmDataLakeStoreFirewallRule parancsmag a megadott adattó-tárolóban kapja meg a megadott tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="56aea-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="56aea-108">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="56aea-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="56aea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56aea-109">EXAMPLES</span></span>

### <span data-ttu-id="56aea-110">Példa 1: adott tűzfalszabály beolvasása</span><span class="sxs-lookup"><span data-stu-id="56aea-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="56aea-111">A "MyFirewallRule" nevű tűzfal-szabályt számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="56aea-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="56aea-112">2. példa: az összes tűzfal-szabály listázása egy fiókban</span><span class="sxs-lookup"><span data-stu-id="56aea-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="56aea-113">A "ContosoADL" fiók minden tűzfal-szabályát visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="56aea-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="56aea-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56aea-114">PARAMETERS</span></span>

### <span data-ttu-id="56aea-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="56aea-115">-Account</span></span>
<span data-ttu-id="56aea-116">Az adattó-tároló fiókja a tűzfalszabály beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="56aea-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="56aea-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56aea-117">-Name</span></span>
<span data-ttu-id="56aea-118">A lekérdezni kívánt tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="56aea-118">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="56aea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56aea-119">-ResourceGroupName</span></span>
<span data-ttu-id="56aea-120">Annak az erőforráscsoport-csoportnak a neve, amely alatt le szeretné olvasni a megadott fiók megadott tűzfalszabályét.</span><span class="sxs-lookup"><span data-stu-id="56aea-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="56aea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56aea-121">-DefaultProfile</span></span>
<span data-ttu-id="56aea-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56aea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56aea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56aea-123">CommonParameters</span></span>
<span data-ttu-id="56aea-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56aea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56aea-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56aea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56aea-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56aea-126">INPUTS</span></span>

## <span data-ttu-id="56aea-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56aea-127">OUTPUTS</span></span>

### <span data-ttu-id="56aea-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="56aea-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="56aea-129">A lekérdezni kívánt tűzfal-szabály</span><span class="sxs-lookup"><span data-stu-id="56aea-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="56aea-130">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="56aea-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="56aea-131">A megadott fiók tűzfal-szabályainak listája.</span><span class="sxs-lookup"><span data-stu-id="56aea-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="56aea-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56aea-132">NOTES</span></span>

## <span data-ttu-id="56aea-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56aea-133">RELATED LINKS</span></span>

