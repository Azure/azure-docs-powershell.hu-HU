---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301352"
---
# <span data-ttu-id="2de44-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2de44-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="2de44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2de44-102">SYNOPSIS</span></span>
<span data-ttu-id="2de44-103">Az értesítési hub névteret hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2de44-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="2de44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2de44-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2de44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2de44-105">DESCRIPTION</span></span>
<span data-ttu-id="2de44-106">A **New-AzNotificationHubsNamespace** parancsmag egy értesítési hub-névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2de44-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="2de44-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="2de44-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="2de44-108">Legalább egy értesítési hub-névtérnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2de44-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="2de44-109">Egyetlen névtérben több hub is berendezhető.</span><span class="sxs-lookup"><span data-stu-id="2de44-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="2de44-110">Több névtér is megszervezhető a hubok rendszerezéséhez, vagy konkrét személyek számára engedélyt adhat a hubok kijelölt részhalmazának kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="2de44-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="2de44-111">Ha névteret szeretne létrehozni, győződjön meg arról, hogy a névtérhez egyedi nevet ad meg; adja meg azt az adatközpontot, ahol a névtér található; adja meg azt az erőforráscsoport-csoportot, amelyhez a névteret hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="2de44-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="2de44-112">Miután létrehozta a névteret, az New-AzNotificationHubsNamespaceAuthorizationRules parancsmagot használva engedélyezési szabályokat rendelhet az adott névtérhez.</span><span class="sxs-lookup"><span data-stu-id="2de44-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="2de44-113">Az engedélyezési szabályok a névtér engedélyeinek kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="2de44-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="2de44-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2de44-114">EXAMPLES</span></span>

### <span data-ttu-id="2de44-115">Példa 1: értesítési központ létrehozása</span><span class="sxs-lookup"><span data-stu-id="2de44-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="2de44-116">Ez a parancs létrehoz egy ContosoPartners nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="2de44-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="2de44-117">A névtér a Nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup-erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="2de44-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="2de44-118">2. példa: értesítési központ létrehozása címkékkel</span><span class="sxs-lookup"><span data-stu-id="2de44-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="2de44-119">Ez a parancs létrehoz egy ContosoPartners nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="2de44-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="2de44-120">A névtér a Nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup-erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="2de44-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="2de44-121">Emellett a parancs létrehoz egy címkét, amely a név célközönsége és az érték PartnerOrganizations, és a névtérhez van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2de44-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="2de44-122">Ez a beállítás biztosítja, hogy a rendszer minden alkalommal megjelenítse a névteret, ha olyan elemeket szűr, amelyek PartnerOrganizations a célközönség címkéje van beállítva.</span><span class="sxs-lookup"><span data-stu-id="2de44-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="2de44-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2de44-123">PARAMETERS</span></span>

### <span data-ttu-id="2de44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de44-124">-DefaultProfile</span></span>
<span data-ttu-id="2de44-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2de44-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2de44-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="2de44-126">-Location</span></span>
<span data-ttu-id="2de44-127">Annak az adatközpontnak a megjelenítendő nevét adja meg, amely a névteret fogja üzemeltetni.</span><span class="sxs-lookup"><span data-stu-id="2de44-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="2de44-128">Bár ezt a paramétert bármilyen érvényes helyre is beállíthatja, hogy optimális legyen, érdemes lehet egy olyan adatközpontot használni, amely a felhasználók többségéhez közel helyezkedik el.</span><span class="sxs-lookup"><span data-stu-id="2de44-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2de44-129">-Namespace</span></span>
<span data-ttu-id="2de44-130">Az új névtér nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2de44-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="2de44-131">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="2de44-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2de44-132">-ResourceGroup</span></span>
<span data-ttu-id="2de44-133">Azt az erőforráscsoport-csoportot adja meg, amelyhez a névteret hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="2de44-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="2de44-134">Az erőforráscsoportok olyan módon rendszerezik az elemeket, mint például a névterek, az értesítési hubok és az engedélyezési szabályok, amelyek megkönnyítik a Készletkezelés és a felügyelet kezelését.</span><span class="sxs-lookup"><span data-stu-id="2de44-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="2de44-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2de44-135">-SkuTier</span></span>
<span data-ttu-id="2de44-136">A névtér SKU-szintjei</span><span class="sxs-lookup"><span data-stu-id="2de44-136">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="2de44-137">-Tag</span></span>
<span data-ttu-id="2de44-138">Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="2de44-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="2de44-139">A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.</span><span class="sxs-lookup"><span data-stu-id="2de44-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="2de44-140">Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.</span><span class="sxs-lookup"><span data-stu-id="2de44-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="2de44-141">Az egyéni címke két részből áll: a *név* és a tetszés szerinti *érték*.</span><span class="sxs-lookup"><span data-stu-id="2de44-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="2de44-142">Például a részlegben: a címke neve részleg, a címke pedig az érték.</span><span class="sxs-lookup"><span data-stu-id="2de44-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="2de44-143">Címke hozzáadásához használja az alábbihoz hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016 címkét hozza létre:</span><span class="sxs-lookup"><span data-stu-id="2de44-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2de44-144">-Confirm</span></span>
<span data-ttu-id="2de44-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2de44-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de44-146">-WhatIf</span></span>
<span data-ttu-id="2de44-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2de44-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2de44-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2de44-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de44-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de44-149">CommonParameters</span></span>
<span data-ttu-id="2de44-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2de44-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de44-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de44-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de44-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de44-152">INPUTS</span></span>

### <span data-ttu-id="2de44-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2de44-153">System.String</span></span>

### <span data-ttu-id="2de44-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2de44-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2de44-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de44-155">OUTPUTS</span></span>

### <span data-ttu-id="2de44-156">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2de44-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="2de44-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2de44-157">NOTES</span></span>

## <span data-ttu-id="2de44-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2de44-158">RELATED LINKS</span></span>

[<span data-ttu-id="2de44-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2de44-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="2de44-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2de44-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="2de44-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2de44-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


