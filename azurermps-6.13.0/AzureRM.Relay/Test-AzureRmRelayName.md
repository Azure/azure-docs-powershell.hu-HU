---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501084"
---
# <span data-ttu-id="1cc1c-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="1cc1c-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="1cc1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc1c-103">A megadott névtér-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1cc1c-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cc1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cc1c-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cc1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cc1c-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc1c-106">A **teszt-AzureRmRelayName** parancsmag a névtér nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="1cc1c-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="1cc1c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1cc1c-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc1c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1cc1c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="1cc1c-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="1cc1c-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="1cc1c-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="1cc1c-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="1cc1c-111">A névtér nevében elérhető állapotot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1cc1c-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="1cc1c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cc1c-112">PARAMETERS</span></span>

### <span data-ttu-id="1cc1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc1c-113">-DefaultProfile</span></span>
<span data-ttu-id="1cc1c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cc1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc1c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1cc1c-115">-Namespace</span></span>
<span data-ttu-id="1cc1c-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="1cc1c-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="1cc1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc1c-117">CommonParameters</span></span>
<span data-ttu-id="1cc1c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cc1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1cc1c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc1c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc1c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cc1c-120">INPUTS</span></span>

### <span data-ttu-id="1cc1c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1cc1c-121">System.String</span></span>


## <span data-ttu-id="1cc1c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cc1c-122">OUTPUTS</span></span>

### <span data-ttu-id="1cc1c-123">Microsoft. Azure. Command. Relay. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="1cc1c-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="1cc1c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cc1c-124">NOTES</span></span>

## <span data-ttu-id="1cc1c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cc1c-125">RELATED LINKS</span></span>
