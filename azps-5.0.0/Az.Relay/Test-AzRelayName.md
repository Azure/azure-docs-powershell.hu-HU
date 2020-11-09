---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300248"
---
# <span data-ttu-id="1826a-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="1826a-101">Test-AzRelayName</span></span>

## <span data-ttu-id="1826a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1826a-102">SYNOPSIS</span></span>
<span data-ttu-id="1826a-103">A megadott névtér-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1826a-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="1826a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1826a-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1826a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1826a-105">DESCRIPTION</span></span>
<span data-ttu-id="1826a-106">A **teszt-AzRelayName** parancsmag a névtér nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="1826a-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="1826a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1826a-107">EXAMPLES</span></span>

### <span data-ttu-id="1826a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1826a-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="1826a-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="1826a-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="1826a-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="1826a-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="1826a-111">A névtér nevében elérhető állapotot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1826a-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="1826a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1826a-112">PARAMETERS</span></span>

### <span data-ttu-id="1826a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1826a-113">-DefaultProfile</span></span>
<span data-ttu-id="1826a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1826a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1826a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1826a-115">-Namespace</span></span>
<span data-ttu-id="1826a-116">A továbbító névtér neve</span><span class="sxs-lookup"><span data-stu-id="1826a-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="1826a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1826a-117">CommonParameters</span></span>
<span data-ttu-id="1826a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1826a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1826a-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1826a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1826a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1826a-120">INPUTS</span></span>

### <span data-ttu-id="1826a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1826a-121">System.String</span></span>

## <span data-ttu-id="1826a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1826a-122">OUTPUTS</span></span>

### <span data-ttu-id="1826a-123">Microsoft. Azure. Command. Relay. models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="1826a-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="1826a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1826a-124">NOTES</span></span>

## <span data-ttu-id="1826a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1826a-125">RELATED LINKS</span></span>
