---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343685"
---
# <span data-ttu-id="0ebd1-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0ebd1-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="0ebd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ebd1-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebd1-103">Beolvassa egy meglévő szabály definícióját egy adott témakör-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="0ebd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ebd1-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ebd1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ebd1-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebd1-106">A **Get-AzServiceBusRule** parancsmag megkapja a témakör adott előfizetésében megadott szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="0ebd1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ebd1-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebd1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ebd1-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="0ebd1-109">Egy adott előfizetéshez megadott szabályleírást ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="0ebd1-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0ebd1-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="0ebd1-111">Visszaadja egy adott előfizetés szabályleírásának listáját.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="0ebd1-112">Alapértelmezés szerint 100 szabályt ad vissza, ha több mint 100 szabályt ad vissza, használja a -MaxCount Parameter paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="0ebd1-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="0ebd1-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="0ebd1-114">Visszaadja egy adott előfizetés első 150 szabályleírásának listáját.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="0ebd1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ebd1-115">PARAMETERS</span></span>

### <span data-ttu-id="0ebd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebd1-116">-DefaultProfile</span></span>
<span data-ttu-id="0ebd1-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebd1-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0ebd1-118">-MaxCount</span></span>
<span data-ttu-id="0ebd1-119">Határozza meg, hogy legfeljebb hány szabályt kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebd1-120">-Name</span></span>
<span data-ttu-id="0ebd1-121">Szabály neve</span><span class="sxs-lookup"><span data-stu-id="0ebd1-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ebd1-122">-Namespace</span></span>
<span data-ttu-id="0ebd1-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0ebd1-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebd1-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ebd1-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0ebd1-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-126">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ebd1-126">-Subscription</span></span>
<span data-ttu-id="0ebd1-127">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="0ebd1-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="0ebd1-128">-Topic</span></span>
<span data-ttu-id="0ebd1-129">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="0ebd1-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebd1-130">CommonParameters</span></span>
<span data-ttu-id="0ebd1-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebd1-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebd1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebd1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ebd1-133">INPUTS</span></span>

### <span data-ttu-id="0ebd1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0ebd1-134">System.String</span></span>

## <span data-ttu-id="0ebd1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ebd1-135">OUTPUTS</span></span>

### <span data-ttu-id="0ebd1-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0ebd1-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0ebd1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ebd1-137">NOTES</span></span>

## <span data-ttu-id="0ebd1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ebd1-138">RELATED LINKS</span></span>
