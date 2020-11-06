---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496856"
---
# <span data-ttu-id="56603-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="56603-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="56603-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56603-102">SYNOPSIS</span></span>
<span data-ttu-id="56603-103">Megkapja a névtér elsődleges és másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="56603-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56603-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56603-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56603-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56603-105">DESCRIPTION</span></span>
<span data-ttu-id="56603-106">A **Get-AzureRmServiceBusNamespaceKey** parancsmag a megadott névtér elsődleges és másodlagos kapcsolati karakterláncát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="56603-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="56603-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56603-107">EXAMPLES</span></span>

### <span data-ttu-id="56603-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56603-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="56603-109">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="56603-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="56603-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56603-110">PARAMETERS</span></span>

### <span data-ttu-id="56603-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56603-111">-ResourceGroup</span></span>
<span data-ttu-id="56603-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="56603-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="56603-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56603-113">-DefaultProfile</span></span>
<span data-ttu-id="56603-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56603-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56603-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56603-115">-Name</span></span>
<span data-ttu-id="56603-116">ServiceBus-névtér AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="56603-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="56603-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="56603-117">-Namespace</span></span>
<span data-ttu-id="56603-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="56603-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="56603-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56603-119">CommonParameters</span></span>
<span data-ttu-id="56603-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56603-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56603-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56603-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56603-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56603-122">INPUTS</span></span>

### <span data-ttu-id="56603-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56603-123">-ResourceGroup</span></span>
 <span data-ttu-id="56603-124">System. String</span><span class="sxs-lookup"><span data-stu-id="56603-124">System.String</span></span>
 

### <span data-ttu-id="56603-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="56603-125">-NamespaceName</span></span>
 <span data-ttu-id="56603-126">System. String</span><span class="sxs-lookup"><span data-stu-id="56603-126">System.String</span></span>
 

### <span data-ttu-id="56603-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="56603-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="56603-128">System. String</span><span class="sxs-lookup"><span data-stu-id="56603-128">System.String</span></span>

## <span data-ttu-id="56603-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56603-129">OUTPUTS</span></span>

### <span data-ttu-id="56603-130">Microsoft. Azure. Management. ServiceBus. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="56603-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="56603-131">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey Value} SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey Value} PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="56603-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="56603-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56603-132">NOTES</span></span>

## <span data-ttu-id="56603-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56603-133">RELATED LINKS</span></span>

