---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195466"
---
# <span data-ttu-id="71e7d-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71e7d-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="71e7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="71e7d-103">Tárolási fiók NetWorkRule tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="71e7d-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="71e7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71e7d-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="71e7d-106">A **Get-AzStorageAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságot kapja meg a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="71e7d-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="71e7d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="71e7d-108">Példa 1: a megadott NetworkRule tulajdonság beolvasása</span><span class="sxs-lookup"><span data-stu-id="71e7d-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="71e7d-109">Ez a parancs a megadott NetworkRule tulajdonságot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71e7d-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="71e7d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71e7d-110">PARAMETERS</span></span>

### <span data-ttu-id="71e7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e7d-111">-DefaultProfile</span></span>
<span data-ttu-id="71e7d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71e7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e7d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71e7d-113">-Name</span></span>
<span data-ttu-id="71e7d-114">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e7d-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="71e7d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e7d-115">-ResourceGroupName</span></span>
<span data-ttu-id="71e7d-116">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="71e7d-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="71e7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e7d-117">CommonParameters</span></span>
<span data-ttu-id="71e7d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71e7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e7d-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e7d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e7d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e7d-120">INPUTS</span></span>

### <span data-ttu-id="71e7d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="71e7d-121">System.String</span></span>

## <span data-ttu-id="71e7d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e7d-122">OUTPUTS</span></span>

### <span data-ttu-id="71e7d-123">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="71e7d-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="71e7d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71e7d-124">NOTES</span></span>

## <span data-ttu-id="71e7d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e7d-125">RELATED LINKS</span></span>
