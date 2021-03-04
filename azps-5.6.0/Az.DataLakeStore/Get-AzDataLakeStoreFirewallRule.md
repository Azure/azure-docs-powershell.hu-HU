---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925946"
---
# <span data-ttu-id="935db-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="935db-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="935db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="935db-102">SYNOPSIS</span></span>
<span data-ttu-id="935db-103">A megadott tűzfalszabályt kapja meg a data lake store-ban.</span><span class="sxs-lookup"><span data-stu-id="935db-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="935db-104">Ha nincs megadva tűzfalszabály, akkor felsorolja a fiók összes tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="935db-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="935db-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="935db-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="935db-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="935db-106">DESCRIPTION</span></span>
<span data-ttu-id="935db-107">A Get-AzDataLakeStoreFirewallRule parancsmag megkapja a megadott tűzfalszabályt a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="935db-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="935db-108">Ha nincs megadva tűzfalszabály, akkor felsorolja a fiók összes tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="935db-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="935db-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="935db-109">EXAMPLES</span></span>

### <span data-ttu-id="935db-110">1. példa: Adott tűzfalszabály beolvasása</span><span class="sxs-lookup"><span data-stu-id="935db-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="935db-111">A "ContosoADL" fiókból visszaadja a MyFirewallRule nevű tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="935db-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="935db-112">2. példa: Egy fiók összes tűzfalszabályának felsorolása</span><span class="sxs-lookup"><span data-stu-id="935db-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="935db-113">Visszaadja a "ContosoADL" fiók összes tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="935db-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="935db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="935db-114">PARAMETERS</span></span>

### <span data-ttu-id="935db-115">-Account</span><span class="sxs-lookup"><span data-stu-id="935db-115">-Account</span></span>
<span data-ttu-id="935db-116">A Data Lake Store-fiók, amelyből beolvassa a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="935db-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="935db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935db-117">-DefaultProfile</span></span>
<span data-ttu-id="935db-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="935db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935db-119">-Name</span><span class="sxs-lookup"><span data-stu-id="935db-119">-Name</span></span>
<span data-ttu-id="935db-120">A visszakeresni megfelelő tűzfalszabály neve</span><span class="sxs-lookup"><span data-stu-id="935db-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="935db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935db-121">-ResourceGroupName</span></span>
<span data-ttu-id="935db-122">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a megadott fiók tűzfalszabályát.</span><span class="sxs-lookup"><span data-stu-id="935db-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="935db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935db-123">CommonParameters</span></span>
<span data-ttu-id="935db-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935db-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935db-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935db-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="935db-126">INPUTS</span></span>

### <span data-ttu-id="935db-127">System.String</span><span class="sxs-lookup"><span data-stu-id="935db-127">System.String</span></span>

## <span data-ttu-id="935db-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="935db-128">OUTPUTS</span></span>

### <span data-ttu-id="935db-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="935db-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="935db-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="935db-130">NOTES</span></span>

## <span data-ttu-id="935db-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="935db-131">RELATED LINKS</span></span>
