---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 88f44a2b399f36f8edf6a57d2f1dc5821029a156
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494387"
---
# <span data-ttu-id="a2147-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="a2147-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="a2147-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2147-102">SYNOPSIS</span></span>
<span data-ttu-id="a2147-103">Frissíti egy HybridConnection leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="a2147-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2147-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2147-104">SYNTAX</span></span>

### <span data-ttu-id="a2147-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2147-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2147-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a2147-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2147-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2147-107">DESCRIPTION</span></span>
<span data-ttu-id="a2147-108">A Set-AzureRmRelayHybridConnection parancsmag a megadott továbbítási névtérben lévő HybridConnection leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="a2147-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="a2147-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2147-109">EXAMPLES</span></span>

### <span data-ttu-id="a2147-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2147-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="a2147-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2147-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="a2147-112">Frissíti a megadott HybridConnection egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="a2147-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="a2147-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="a2147-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="a2147-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2147-114">PARAMETERS</span></span>

### <span data-ttu-id="a2147-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2147-115">-DefaultProfile</span></span>
<span data-ttu-id="a2147-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2147-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2147-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2147-117">-InputObject</span></span>
<span data-ttu-id="a2147-118">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="a2147-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2147-119">-Name</span></span>
<span data-ttu-id="a2147-120">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="a2147-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a2147-121">-Namespace</span></span>
<span data-ttu-id="a2147-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a2147-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2147-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2147-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a2147-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="a2147-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a2147-125">-UserMetadata</span></span>
<span data-ttu-id="a2147-126">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="a2147-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2147-127">-Confirm</span></span>
<span data-ttu-id="a2147-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2147-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2147-129">-WhatIf</span></span>
<span data-ttu-id="a2147-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2147-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2147-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2147-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2147-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2147-132">CommonParameters</span></span>
<span data-ttu-id="a2147-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2147-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2147-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2147-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2147-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2147-135">INPUTS</span></span>

### <span data-ttu-id="a2147-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2147-136">-ResourceGroupName</span></span>
<span data-ttu-id="a2147-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a2147-137">System.String</span></span>

### <span data-ttu-id="a2147-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a2147-138">-NamespaceName</span></span>
<span data-ttu-id="a2147-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a2147-139">System.String</span></span>

### <span data-ttu-id="a2147-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="a2147-140">-WcfRelayName</span></span>
<span data-ttu-id="a2147-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a2147-141">System.String</span></span>

### <span data-ttu-id="a2147-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2147-142">-InputObject</span></span>
<span data-ttu-id="a2147-143">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="a2147-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="a2147-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a2147-144">-UserMetadata</span></span>
<span data-ttu-id="a2147-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a2147-145">System.String</span></span>

## <span data-ttu-id="a2147-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2147-146">OUTPUTS</span></span>

### <span data-ttu-id="a2147-147">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="a2147-147">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="a2147-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2147-148">NOTES</span></span>

## <span data-ttu-id="a2147-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2147-149">RELATED LINKS</span></span>

