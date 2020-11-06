---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498871"
---
# <span data-ttu-id="b8012-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="b8012-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="b8012-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8012-102">SYNOPSIS</span></span>
<span data-ttu-id="b8012-103">A megadott névtér-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="b8012-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8012-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8012-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8012-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8012-105">DESCRIPTION</span></span>
<span data-ttu-id="b8012-106">A **teszt-AzureRmRelayName** parancsmag a névtér nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="b8012-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="b8012-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8012-107">EXAMPLES</span></span>

### <span data-ttu-id="b8012-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8012-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="b8012-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="b8012-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="b8012-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="b8012-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="b8012-111">A névtér nevében elérhető állapotot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b8012-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="b8012-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8012-112">PARAMETERS</span></span>

### <span data-ttu-id="b8012-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8012-113">-DefaultProfile</span></span>
<span data-ttu-id="b8012-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8012-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8012-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8012-115">-Namespace</span></span>
<span data-ttu-id="b8012-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="b8012-116">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8012-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8012-117">CommonParameters</span></span>
<span data-ttu-id="b8012-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8012-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8012-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8012-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8012-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8012-120">INPUTS</span></span>

### <span data-ttu-id="b8012-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8012-121">-Namespace</span></span>
 <span data-ttu-id="b8012-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b8012-122">System.String</span></span>

## <span data-ttu-id="b8012-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8012-123">OUTPUTS</span></span>

### <span data-ttu-id="b8012-124">[Microsoft. Azure. Command. Relay. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="b8012-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="b8012-125">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8012-125">Example 1</span></span>
<span data-ttu-id="b8012-126">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="b8012-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="b8012-127">2. példa</span><span class="sxs-lookup"><span data-stu-id="b8012-127">Example 2</span></span>
<span data-ttu-id="b8012-128">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="b8012-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="b8012-129">3. példa</span><span class="sxs-lookup"><span data-stu-id="b8012-129">Example 3</span></span>
<span data-ttu-id="b8012-130">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="b8012-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="b8012-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8012-131">NOTES</span></span>

## <span data-ttu-id="b8012-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8012-132">RELATED LINKS</span></span>

