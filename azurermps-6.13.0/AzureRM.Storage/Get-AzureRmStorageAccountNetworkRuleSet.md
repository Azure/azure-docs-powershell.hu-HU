---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495583"
---
# <span data-ttu-id="f8f5c-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8f5c-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f8f5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f5c-103">Tárolási fiók NetWorkRule tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f8f5c-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8f5c-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f5c-106">A **Get-AzureRmStorageAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságot kapja meg a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="f8f5c-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f8f5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f8f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="f8f5c-108">Példa 1: a megadott NetworkRule tulajdonság beolvasása</span><span class="sxs-lookup"><span data-stu-id="f8f5c-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="f8f5c-109">Ez a parancs a megadott NetworkRule tulajdonságot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8f5c-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="f8f5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="f8f5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f5c-111">-DefaultProfile</span></span>
<span data-ttu-id="f8f5c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8f5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f5c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f8f5c-113">-Name</span></span>
<span data-ttu-id="f8f5c-114">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8f5c-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f8f5c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f5c-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8f5c-116">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="f8f5c-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f8f5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f5c-117">CommonParameters</span></span>
<span data-ttu-id="f8f5c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8f5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f5c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f5c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f5c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8f5c-120">INPUTS</span></span>

### <span data-ttu-id="f8f5c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f8f5c-121">System.String</span></span>

## <span data-ttu-id="f8f5c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8f5c-122">OUTPUTS</span></span>

### <span data-ttu-id="f8f5c-123">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8f5c-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f8f5c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8f5c-124">NOTES</span></span>

## <span data-ttu-id="f8f5c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8f5c-125">RELATED LINKS</span></span>
