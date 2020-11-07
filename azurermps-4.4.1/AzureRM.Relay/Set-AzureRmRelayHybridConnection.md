---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679046"
---
# <span data-ttu-id="8888d-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="8888d-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="8888d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8888d-102">SYNOPSIS</span></span>
<span data-ttu-id="8888d-103">Frissíti egy HybridConnection leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="8888d-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8888d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8888d-104">SYNTAX</span></span>

### <span data-ttu-id="8888d-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8888d-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8888d-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8888d-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8888d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8888d-107">DESCRIPTION</span></span>
<span data-ttu-id="8888d-108">A Set-AzureRmRelayHybridConnection parancsmag a megadott továbbítási névtérben lévő HybridConnection leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="8888d-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8888d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8888d-109">EXAMPLES</span></span>

### <span data-ttu-id="8888d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8888d-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="8888d-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="8888d-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="8888d-112">Frissíti a megadott HybridConnection egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="8888d-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="8888d-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="8888d-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="8888d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8888d-114">PARAMETERS</span></span>

### <span data-ttu-id="8888d-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8888d-115">-UserMetadata</span></span>
<span data-ttu-id="8888d-116">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="8888d-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8888d-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8888d-117">-Confirm</span></span>
<span data-ttu-id="8888d-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8888d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8888d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8888d-119">-WhatIf</span></span>
<span data-ttu-id="8888d-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8888d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8888d-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8888d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8888d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8888d-122">-InputObject</span></span>
<span data-ttu-id="8888d-123">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="8888d-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8888d-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8888d-124">-Name</span></span>
<span data-ttu-id="8888d-125">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="8888d-125">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8888d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8888d-126">-Namespace</span></span>
<span data-ttu-id="8888d-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8888d-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8888d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8888d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8888d-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8888d-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8888d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8888d-130">-DefaultProfile</span></span>
<span data-ttu-id="8888d-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8888d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8888d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8888d-132">CommonParameters</span></span>
<span data-ttu-id="8888d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8888d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8888d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8888d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8888d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8888d-135">INPUTS</span></span>

### <span data-ttu-id="8888d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8888d-136">-ResourceGroupName</span></span>
<span data-ttu-id="8888d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8888d-137">System.String</span></span>

### <span data-ttu-id="8888d-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8888d-138">-NamespaceName</span></span>
<span data-ttu-id="8888d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8888d-139">System.String</span></span>

### <span data-ttu-id="8888d-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="8888d-140">-WcfRelayName</span></span>
<span data-ttu-id="8888d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8888d-141">System.String</span></span>

### <span data-ttu-id="8888d-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8888d-142">-InputObject</span></span>
<span data-ttu-id="8888d-143">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="8888d-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="8888d-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8888d-144">-UserMetadata</span></span>
<span data-ttu-id="8888d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8888d-145">System.String</span></span>

## <span data-ttu-id="8888d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8888d-146">OUTPUTS</span></span>

### <span data-ttu-id="8888d-147">Példák-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="8888d-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="8888d-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: teszt UserMetadata azonosító:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 név: TestHybirdConnection2 típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="8888d-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="8888d-149">Példák-2: tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="8888d-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="8888d-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: teszt UserMetadata frissítve ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 név: TestHybirdConnection1 típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="8888d-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="8888d-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8888d-151">NOTES</span></span>

## <span data-ttu-id="8888d-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8888d-152">RELATED LINKS</span></span>

