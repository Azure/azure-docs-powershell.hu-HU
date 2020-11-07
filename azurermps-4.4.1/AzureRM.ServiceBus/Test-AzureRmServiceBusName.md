---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679935"
---
# <span data-ttu-id="113be-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="113be-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="113be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="113be-102">SYNOPSIS</span></span>
<span data-ttu-id="113be-103">A megadott névtér-név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="113be-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="113be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="113be-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="113be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="113be-105">DESCRIPTION</span></span>
<span data-ttu-id="113be-106">A **teszt-AzureRmServiceBusName** parancsmag a névtér nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="113be-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="113be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="113be-107">EXAMPLES</span></span>

### <span data-ttu-id="113be-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="113be-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="113be-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="113be-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="113be-110">3. példa</span><span class="sxs-lookup"><span data-stu-id="113be-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="113be-111">A névtér nevében elérhető állapotot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="113be-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="113be-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="113be-112">PARAMETERS</span></span>

### <span data-ttu-id="113be-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="113be-113">-Namespace</span></span>
<span data-ttu-id="113be-114">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="113be-114">ServiceBus Namespace Name.</span></span>

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
### <span data-ttu-id="113be-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113be-115">CommonParameters</span></span>
<span data-ttu-id="113be-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="113be-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113be-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="113be-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113be-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="113be-118">INPUTS</span></span>

### <span data-ttu-id="113be-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="113be-119">-Namespace</span></span>
 <span data-ttu-id="113be-120">System. String</span><span class="sxs-lookup"><span data-stu-id="113be-120">System.String</span></span>

## <span data-ttu-id="113be-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="113be-121">OUTPUTS</span></span>

### <span data-ttu-id="113be-122">[Microsoft. Azure. Command. ServiceBus. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="113be-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="113be-123">Példa 1</span><span class="sxs-lookup"><span data-stu-id="113be-123">Example 1</span></span>
<span data-ttu-id="113be-124">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="113be-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="113be-125">2. példa</span><span class="sxs-lookup"><span data-stu-id="113be-125">Example 2</span></span>
<span data-ttu-id="113be-126">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="113be-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="113be-127">3. példa</span><span class="sxs-lookup"><span data-stu-id="113be-127">Example 3</span></span>
<span data-ttu-id="113be-128">NameAvailable-ok üzenet</span><span class="sxs-lookup"><span data-stu-id="113be-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="113be-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="113be-129">NOTES</span></span>

## <span data-ttu-id="113be-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="113be-130">RELATED LINKS</span></span>
