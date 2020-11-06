---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500696"
---
# <span data-ttu-id="f809e-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f809e-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="f809e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f809e-102">SYNOPSIS</span></span>
<span data-ttu-id="f809e-103">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a Service Bus névtérhez.</span><span class="sxs-lookup"><span data-stu-id="f809e-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f809e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f809e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f809e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f809e-105">DESCRIPTION</span></span>
<span data-ttu-id="f809e-106">A **New-AzureRmServiceBusNamespace** parancsmag új elsődleges vagy másodlagos csatlakozási karakterláncokat hoz létre a megadott névtér-és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="f809e-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="f809e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f809e-107">EXAMPLES</span></span>

### <span data-ttu-id="f809e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f809e-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="f809e-109">Újragenerálja a névtér elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="f809e-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="f809e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f809e-110">PARAMETERS</span></span>

### <span data-ttu-id="f809e-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f809e-111">-RegenerateKeys</span></span>
<span data-ttu-id="f809e-112">Újragenerálási kulcsok: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="f809e-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f809e-113">-ResourceGroup</span></span>
<span data-ttu-id="f809e-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f809e-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f809e-115">-Confirm</span></span>
<span data-ttu-id="f809e-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f809e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f809e-117">-WhatIf</span></span>
<span data-ttu-id="f809e-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f809e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f809e-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f809e-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f809e-120">-DefaultProfile</span></span>
<span data-ttu-id="f809e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f809e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f809e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f809e-122">-Name</span></span>
<span data-ttu-id="f809e-123">Engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="f809e-123">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f809e-124">-Namespace</span></span>
<span data-ttu-id="f809e-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f809e-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f809e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f809e-126">CommonParameters</span></span>
<span data-ttu-id="f809e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f809e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f809e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f809e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f809e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f809e-129">INPUTS</span></span>

### <span data-ttu-id="f809e-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f809e-130">-ResourceGroup</span></span>
 <span data-ttu-id="f809e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f809e-131">System.String</span></span>
 

### <span data-ttu-id="f809e-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f809e-132">-NamespaceName</span></span>
 <span data-ttu-id="f809e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f809e-133">System.String</span></span>
 

### <span data-ttu-id="f809e-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f809e-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f809e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f809e-135">System.String</span></span>
 

### <span data-ttu-id="f809e-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f809e-136">-RegenerateKeys</span></span>
 <span data-ttu-id="f809e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f809e-137">System.String</span></span>

## <span data-ttu-id="f809e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f809e-138">OUTPUTS</span></span>

### <span data-ttu-id="f809e-139">Microsoft. Azure. Management. ServiceBus. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="f809e-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="f809e-140">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f809e-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="f809e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f809e-141">NOTES</span></span>

## <span data-ttu-id="f809e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f809e-142">RELATED LINKS</span></span>

