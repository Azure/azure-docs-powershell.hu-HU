---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010500"
---
# <span data-ttu-id="4c286-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4c286-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4c286-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c286-102">SYNOPSIS</span></span>
<span data-ttu-id="4c286-103">A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="4c286-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4c286-104">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="4c286-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="4c286-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c286-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c286-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c286-106">DESCRIPTION</span></span>
<span data-ttu-id="4c286-107">A Get-AzDataLakeStoreFirewallRule parancsmag a megadott adattó-tárolóban kapja meg a megadott tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="4c286-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="4c286-108">Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.</span><span class="sxs-lookup"><span data-stu-id="4c286-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="4c286-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4c286-109">EXAMPLES</span></span>

### <span data-ttu-id="4c286-110">Példa 1: adott tűzfalszabály beolvasása</span><span class="sxs-lookup"><span data-stu-id="4c286-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="4c286-111">A "MyFirewallRule" nevű tűzfal-szabályt számítja ki a "ContosoADL" fiókból.</span><span class="sxs-lookup"><span data-stu-id="4c286-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="4c286-112">2. példa: az összes tűzfal-szabály listázása egy fiókban</span><span class="sxs-lookup"><span data-stu-id="4c286-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="4c286-113">A "ContosoADL" fiók minden tűzfal-szabályát visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="4c286-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="4c286-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c286-114">PARAMETERS</span></span>

### <span data-ttu-id="4c286-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4c286-115">-Account</span></span>
<span data-ttu-id="4c286-116">Az adattó-tároló fiókja a tűzfalszabály beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="4c286-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="4c286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c286-117">-DefaultProfile</span></span>
<span data-ttu-id="4c286-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c286-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c286-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c286-119">-Name</span></span>
<span data-ttu-id="4c286-120">A lekérdezni kívánt tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="4c286-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="4c286-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c286-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c286-122">Annak az erőforráscsoport-csoportnak a neve, amely alatt le szeretné olvasni a megadott fiók megadott tűzfalszabályét.</span><span class="sxs-lookup"><span data-stu-id="4c286-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="4c286-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c286-123">CommonParameters</span></span>
<span data-ttu-id="4c286-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c286-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c286-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c286-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c286-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c286-126">INPUTS</span></span>

### <span data-ttu-id="4c286-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4c286-127">System.String</span></span>

## <span data-ttu-id="4c286-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c286-128">OUTPUTS</span></span>

### <span data-ttu-id="4c286-129">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4c286-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="4c286-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c286-130">NOTES</span></span>

## <span data-ttu-id="4c286-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c286-131">RELATED LINKS</span></span>
