---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: ca477e278ef28cd2fce17578d55782f3ab610954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000629"
---
# <span data-ttu-id="1c39d-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="1c39d-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="1c39d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c39d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c39d-103">A megadott továbbítási entitások (Namespace/WcfRelay/HybridConnection) elsődleges és másodlagos kapcsolati karakterláncának lekérte.</span><span class="sxs-lookup"><span data-stu-id="1c39d-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1c39d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c39d-104">SYNTAX</span></span>

### <span data-ttu-id="1c39d-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c39d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c39d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c39d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c39d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c39d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c39d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c39d-108">DESCRIPTION</span></span>
<span data-ttu-id="1c39d-109">A **Get-AzRelayKey** parancsmag a megadott továbbítási entitások (Namespace/WcfRelay/HybridConnection) elsődleges és másodlagos kapcsolati karakterláncát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1c39d-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1c39d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c39d-110">EXAMPLES</span></span>

### <span data-ttu-id="1c39d-111">1. példa: Namespace</span><span class="sxs-lookup"><span data-stu-id="1c39d-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="1c39d-112">2. példa: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1c39d-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="1c39d-113">3. példa: Hibrid összekapcsolás</span><span class="sxs-lookup"><span data-stu-id="1c39d-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="1c39d-114">Elsődleges és másodlagos kapcsolati karakterlánc a megadott továbbítási entitásokkal (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="1c39d-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1c39d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c39d-115">PARAMETERS</span></span>

### <span data-ttu-id="1c39d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c39d-116">-DefaultProfile</span></span>
<span data-ttu-id="1c39d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c39d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c39d-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1c39d-118">-HybridConnection</span></span>
<span data-ttu-id="1c39d-119">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="1c39d-119">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c39d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c39d-120">-Name</span></span>
<span data-ttu-id="1c39d-121">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="1c39d-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c39d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1c39d-122">-Namespace</span></span>
<span data-ttu-id="1c39d-123">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="1c39d-123">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c39d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c39d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c39d-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c39d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c39d-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1c39d-126">-WcfRelay</span></span>
<span data-ttu-id="1c39d-127">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="1c39d-127">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c39d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c39d-128">CommonParameters</span></span>
<span data-ttu-id="1c39d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c39d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c39d-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c39d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c39d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c39d-131">INPUTS</span></span>

### <span data-ttu-id="1c39d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1c39d-132">System.String</span></span>

## <span data-ttu-id="1c39d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c39d-133">OUTPUTS</span></span>

### <span data-ttu-id="1c39d-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1c39d-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="1c39d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c39d-135">NOTES</span></span>

## <span data-ttu-id="1c39d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c39d-136">RELATED LINKS</span></span>
