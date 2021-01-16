---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479595"
---
# <span data-ttu-id="fe9b5-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="fe9b5-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="fe9b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9b5-103">A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve)</span><span class="sxs-lookup"><span data-stu-id="fe9b5-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="fe9b5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe9b5-104">SYNTAX</span></span>

### <span data-ttu-id="fe9b5-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe9b5-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe9b5-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe9b5-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9b5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe9b5-107">DESCRIPTION</span></span>
<span data-ttu-id="fe9b5-108">A **Test-AzServiceBusName parancsmag** ellenőrzi, hogy rendelkezésre áll-e a NameSpace név vagy alias (DR konfigurációneve)</span><span class="sxs-lookup"><span data-stu-id="fe9b5-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="fe9b5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe9b5-109">EXAMPLES</span></span>

### <span data-ttu-id="fe9b5-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="fe9b5-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="fe9b5-111">A "MyNameSapceName" név elérhetőségének állapotát adja vissza Igaz értékként.</span><span class="sxs-lookup"><span data-stu-id="fe9b5-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="fe9b5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fe9b5-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="fe9b5-113">A "MyNameSapceName" név "MyNameSapceName" elérhetőségének állapotát adja vissza hamisként, ok nélkül.</span><span class="sxs-lookup"><span data-stu-id="fe9b5-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="fe9b5-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="fe9b5-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="fe9b5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe9b5-115">PARAMETERS</span></span>

### <span data-ttu-id="fe9b5-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fe9b5-116">-AliasName</span></span>
<span data-ttu-id="fe9b5-117">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="fe9b5-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9b5-118">-DefaultProfile</span></span>
<span data-ttu-id="fe9b5-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe9b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9b5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe9b5-120">-Namespace</span></span>
<span data-ttu-id="fe9b5-121">Servicebus Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fe9b5-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe9b5-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fe9b5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9b5-124">CommonParameters</span></span>
<span data-ttu-id="fe9b5-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9b5-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9b5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9b5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9b5-127">INPUTS</span></span>

### <span data-ttu-id="fe9b5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fe9b5-128">System.String</span></span>

## <span data-ttu-id="fe9b5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe9b5-129">OUTPUTS</span></span>

### <span data-ttu-id="fe9b5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="fe9b5-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="fe9b5-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe9b5-131">NOTES</span></span>

## <span data-ttu-id="fe9b5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe9b5-132">RELATED LINKS</span></span>
