---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848990"
---
# <span data-ttu-id="737fe-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="737fe-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="737fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="737fe-102">SYNOPSIS</span></span>
<span data-ttu-id="737fe-103">Tárolási fiók NetWorkRule tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="737fe-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="737fe-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="737fe-105">DESCRIPTION</span></span>
<span data-ttu-id="737fe-106">A **Get-AzureRmStorageAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságot kapja meg a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="737fe-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="737fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="737fe-107">EXAMPLES</span></span>

### <span data-ttu-id="737fe-108">Példa 1: a megadott NetworkRule tulajdonság beolvasása</span><span class="sxs-lookup"><span data-stu-id="737fe-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="737fe-109">Ez a parancs a megadott NetworkRule tulajdonságot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="737fe-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="737fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="737fe-110">PARAMETERS</span></span>

### <span data-ttu-id="737fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737fe-111">-DefaultProfile</span></span>
<span data-ttu-id="737fe-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="737fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737fe-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="737fe-113">-Name</span></span>
<span data-ttu-id="737fe-114">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="737fe-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="737fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="737fe-116">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="737fe-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="737fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737fe-117">CommonParameters</span></span>
<span data-ttu-id="737fe-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="737fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737fe-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737fe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737fe-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="737fe-120">INPUTS</span></span>

### <span data-ttu-id="737fe-121">System. String</span><span class="sxs-lookup"><span data-stu-id="737fe-121">System.String</span></span>

## <span data-ttu-id="737fe-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="737fe-122">OUTPUTS</span></span>

### <span data-ttu-id="737fe-123">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="737fe-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="737fe-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="737fe-124">NOTES</span></span>

## <span data-ttu-id="737fe-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="737fe-125">RELATED LINKS</span></span>
