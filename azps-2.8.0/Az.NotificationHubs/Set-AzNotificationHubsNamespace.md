---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 9a17dfd649f35da3fa071eb7c6d2752d3a923398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838491"
---
# <span data-ttu-id="e3476-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e3476-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="e3476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3476-102">SYNOPSIS</span></span>
<span data-ttu-id="e3476-103">Az értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="e3476-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="e3476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3476-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3476-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3476-105">DESCRIPTION</span></span>
<span data-ttu-id="e3476-106">A **set-AzNotificationHubsNamespace** parancsmag a meglévő értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="e3476-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="e3476-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="e3476-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="e3476-108">Legalább egy értesítési hub-névtérnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e3476-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="e3476-109">Emellett minden értesítési hub-nak rendelkeznie kell hozzárendelt névtérrel.</span><span class="sxs-lookup"><span data-stu-id="e3476-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="e3476-110">Ez a parancsmag elsősorban a névterek engedélyezéséhez és letiltásához használatos.</span><span class="sxs-lookup"><span data-stu-id="e3476-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="e3476-111">Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtérben lévő értesítési hubokhoz, és a rendszergazdák ezekkel a hubok segítségével küldhetnek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="e3476-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="e3476-112">Ha újra engedélyezni szeretné egy letiltott névtér használatát, ezzel a parancsmaggal állítsa be az aktív névtér **állapot** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="e3476-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="e3476-113">Ezt a parancsmagot is megadhatja kritikusként a névtér címkézéséhez.</span><span class="sxs-lookup"><span data-stu-id="e3476-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="e3476-114">Ez a beállítás megakadályozza a névtér törlését.</span><span class="sxs-lookup"><span data-stu-id="e3476-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="e3476-115">A kritikus névterek eltávolításához előbb el kell távolítania a kritikus címkét.</span><span class="sxs-lookup"><span data-stu-id="e3476-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="e3476-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e3476-116">EXAMPLES</span></span>

### <span data-ttu-id="e3476-117">Példa 1: névtér letiltása</span><span class="sxs-lookup"><span data-stu-id="e3476-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="e3476-118">Ez a parancs letiltja a ContosoPartners nevű névteret a West US Datacenter-ben, és a ContosoNotificationsGroup-erőforráscsoport számára van társítva.</span><span class="sxs-lookup"><span data-stu-id="e3476-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="e3476-119">2. példa: névtér engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e3476-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="e3476-120">Ez a parancs lehetővé teszi, hogy a ContosoPartners nevű névtér a West US-adatközpontban található, és a ContosoNotificationsGroup erőforráscsoport legyen társítva.</span><span class="sxs-lookup"><span data-stu-id="e3476-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="e3476-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3476-121">PARAMETERS</span></span>

### <span data-ttu-id="e3476-122">-Kritikus</span><span class="sxs-lookup"><span data-stu-id="e3476-122">-Critical</span></span>
<span data-ttu-id="e3476-123">Azt jelzi, hogy a névtér a kritikus névtér-e.</span><span class="sxs-lookup"><span data-stu-id="e3476-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="e3476-124">A kritikus névterek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="e3476-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="e3476-125">A kritikus névterek törléséhez a tulajdonság értékét false értékre kell állítania ahhoz, hogy a névteret nem kritikusként jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="e3476-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3476-126">-DefaultProfile</span></span>
<span data-ttu-id="e3476-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3476-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3476-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e3476-128">-Force</span></span>
<span data-ttu-id="e3476-129">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3476-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="e3476-130">-Location</span></span>
<span data-ttu-id="e3476-131">A névteret működtető adatközpont megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3476-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="e3476-132">Bár ezt a paramétert bármely érvényes Azure-helyre beállíthatja, így optimális teljesítményhez a felhasználók többségéhez közeli adatközpontot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="e3476-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="e3476-133">Az Azure-helyek naprakész listáját az alábbi parancs futtatásával érheti el: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="e3476-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="e3476-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3476-134">-Namespace</span></span>
<span data-ttu-id="e3476-135">A parancsmag által módosított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3476-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="e3476-136">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="e3476-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e3476-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3476-137">-ResourceGroup</span></span>
<span data-ttu-id="e3476-138">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="e3476-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="e3476-139">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="e3476-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e3476-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e3476-140">-SkuTier</span></span>
<span data-ttu-id="e3476-141">A névtér SKU-szintjei</span><span class="sxs-lookup"><span data-stu-id="e3476-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="e3476-142">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e3476-142">-State</span></span>
<span data-ttu-id="e3476-143">A névtér aktuális állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3476-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="e3476-144">A paraméter elfogadható értékei a következők: aktív és le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="e3476-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="e3476-145">-Tag</span></span>
<span data-ttu-id="e3476-146">Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3476-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="e3476-147">A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.</span><span class="sxs-lookup"><span data-stu-id="e3476-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="e3476-148">Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.</span><span class="sxs-lookup"><span data-stu-id="e3476-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="e3476-149">Az egyéni címke két részből áll: a *név* és (tetszés szerint) az *érték*.</span><span class="sxs-lookup"><span data-stu-id="e3476-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="e3476-150">A részlegben például a címke neve részleg, a címke pedig az érték.</span><span class="sxs-lookup"><span data-stu-id="e3476-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="e3476-151">Címke hozzáadásához használja az ehhez hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016:-Tags @ {Name = "CalendarYear" kifejezést hozza létre. Value = "2016"} Ha több címkét szeretne hozzáadni ugyanabba a parancsba, válassza el az egyes címkéket vesszőkkel: – címke @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "pénzügyi év időszaka"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="e3476-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3476-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3476-152">-Confirm</span></span>
<span data-ttu-id="e3476-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3476-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3476-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3476-154">-WhatIf</span></span>
<span data-ttu-id="e3476-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3476-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3476-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3476-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3476-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3476-157">CommonParameters</span></span>
<span data-ttu-id="e3476-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3476-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3476-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3476-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3476-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3476-160">INPUTS</span></span>

### <span data-ttu-id="e3476-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e3476-161">System.String</span></span>

### <span data-ttu-id="e3476-162">Microsoft. Azure. Command. NotificationHubs. models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="e3476-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="e3476-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3476-163">System.Boolean</span></span>

### <span data-ttu-id="e3476-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3476-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3476-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3476-165">OUTPUTS</span></span>

### <span data-ttu-id="e3476-166">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e3476-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e3476-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3476-167">NOTES</span></span>

## <span data-ttu-id="e3476-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3476-168">RELATED LINKS</span></span>

[<span data-ttu-id="e3476-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e3476-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e3476-170">Új – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e3476-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e3476-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e3476-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


