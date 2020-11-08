---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011246"
---
# <span data-ttu-id="6cb7a-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6cb7a-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6cb7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb7a-103">Tárolási fiók NetWorkRule tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6cb7a-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="6cb7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cb7a-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cb7a-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb7a-106">A **Get-AzStorageAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságot kapja meg a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="6cb7a-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="6cb7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6cb7a-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb7a-108">Példa 1: a megadott NetworkRule tulajdonság beolvasása</span><span class="sxs-lookup"><span data-stu-id="6cb7a-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="6cb7a-109">Ez a parancs a megadott NetworkRule tulajdonságot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="6cb7a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cb7a-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb7a-111">-DefaultProfile</span></span>
<span data-ttu-id="6cb7a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb7a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cb7a-113">-Name</span></span>
<span data-ttu-id="6cb7a-114">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb7a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6cb7a-116">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-116">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb7a-117">CommonParameters</span></span>
<span data-ttu-id="6cb7a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cb7a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb7a-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb7a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb7a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb7a-120">INPUTS</span></span>

### <span data-ttu-id="6cb7a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb7a-121">System.String</span></span>

## <span data-ttu-id="6cb7a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cb7a-122">OUTPUTS</span></span>

### <span data-ttu-id="6cb7a-123">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6cb7a-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6cb7a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cb7a-124">NOTES</span></span>

## <span data-ttu-id="6cb7a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cb7a-125">RELATED LINKS</span></span>
