---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345329"
---
# <span data-ttu-id="438b7-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="438b7-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="438b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="438b7-102">SYNOPSIS</span></span>
<span data-ttu-id="438b7-103">A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve)</span><span class="sxs-lookup"><span data-stu-id="438b7-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="438b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="438b7-104">SYNTAX</span></span>

### <span data-ttu-id="438b7-105">NamespaceCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="438b7-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="438b7-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="438b7-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="438b7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="438b7-107">DESCRIPTION</span></span>
<span data-ttu-id="438b7-108">A **Test-AzEventhubName parancsmag** ellenőrzi, hogy rendelkezésre áll-e a NameSpace név vagy alias (DR configuration name)</span><span class="sxs-lookup"><span data-stu-id="438b7-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="438b7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="438b7-109">EXAMPLES</span></span>

### <span data-ttu-id="438b7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="438b7-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="438b7-111">A "MyNameSapceName" név elérhetőségének állapotát adja vissza Igaz értékként, ha elérhető.</span><span class="sxs-lookup"><span data-stu-id="438b7-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="438b7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="438b7-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="438b7-113">A "MyNameSapceName" név "MyNameSapceName" elérhetőségének állapotát adja vissza hamisként, ok nélkül.</span><span class="sxs-lookup"><span data-stu-id="438b7-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="438b7-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="438b7-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="438b7-115">A "MyNameSapceName" névtér "MyNameSapceName" aliasának elérhetőségi állapotát adja vissza Igaz értékként, ha elérhető.</span><span class="sxs-lookup"><span data-stu-id="438b7-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="438b7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="438b7-116">PARAMETERS</span></span>

### <span data-ttu-id="438b7-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="438b7-117">-AliasName</span></span>
<span data-ttu-id="438b7-118">DR Configuration Name - Alias Name</span><span class="sxs-lookup"><span data-stu-id="438b7-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="438b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438b7-119">-DefaultProfile</span></span>
<span data-ttu-id="438b7-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="438b7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="438b7-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="438b7-121">-Namespace</span></span>
<span data-ttu-id="438b7-122">Eventhub Namespace Name</span><span class="sxs-lookup"><span data-stu-id="438b7-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="438b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="438b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="438b7-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="438b7-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="438b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438b7-125">CommonParameters</span></span>
<span data-ttu-id="438b7-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438b7-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438b7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438b7-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="438b7-128">INPUTS</span></span>

### <span data-ttu-id="438b7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="438b7-129">System.String</span></span>

## <span data-ttu-id="438b7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="438b7-130">OUTPUTS</span></span>

### <span data-ttu-id="438b7-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="438b7-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="438b7-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="438b7-132">NOTES</span></span>

## <span data-ttu-id="438b7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="438b7-133">RELATED LINKS</span></span>
