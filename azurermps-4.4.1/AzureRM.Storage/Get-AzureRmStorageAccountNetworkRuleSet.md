---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680739"
---
# <span data-ttu-id="d47d9-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d47d9-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d47d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d47d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d47d9-103">Tárolási fiók NetWorkRule tulajdonságának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d47d9-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d47d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d47d9-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d47d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d47d9-105">DESCRIPTION</span></span>
<span data-ttu-id="d47d9-106">A **Get-AzureRmStorageAccountNetworkRuleSet** parancsmag a NetworkRule tulajdonságot kapja meg a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="d47d9-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="d47d9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d47d9-107">EXAMPLES</span></span>

### <span data-ttu-id="d47d9-108">Példa 1: a megadott NetworkRule tulajdonság beolvasása</span><span class="sxs-lookup"><span data-stu-id="d47d9-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="d47d9-109">Ez a parancs a megadott NetworkRule tulajdonságot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d47d9-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="d47d9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d47d9-110">PARAMETERS</span></span>

### <span data-ttu-id="d47d9-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d47d9-111">-Name</span></span>
<span data-ttu-id="d47d9-112">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d47d9-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d47d9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d47d9-113">-ResourceGroupName</span></span>
<span data-ttu-id="d47d9-114">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="d47d9-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d47d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d47d9-115">-DefaultProfile</span></span>
<span data-ttu-id="d47d9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d47d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d47d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d47d9-117">CommonParameters</span></span>
<span data-ttu-id="d47d9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d47d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d47d9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d47d9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d47d9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d47d9-120">INPUTS</span></span>

### <span data-ttu-id="d47d9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d47d9-121">System.String</span></span>

## <span data-ttu-id="d47d9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d47d9-122">OUTPUTS</span></span>

### <span data-ttu-id="d47d9-123">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d47d9-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d47d9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d47d9-124">NOTES</span></span>

## <span data-ttu-id="d47d9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d47d9-125">RELATED LINKS</span></span>

