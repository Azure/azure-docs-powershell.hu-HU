---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 90fbdc94c372cbe02aaecde4ff27ad28dcec8e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494770"
---
# <span data-ttu-id="72dfd-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72dfd-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="72dfd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="72dfd-103">Az értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="72dfd-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dfd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72dfd-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tags] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dfd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="72dfd-106">A **set-AzureRmNotificationHubsNamespace** parancsmag a meglévő értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="72dfd-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>

<span data-ttu-id="72dfd-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="72dfd-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="72dfd-108">Legalább egy értesítési hub-névtérnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="72dfd-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="72dfd-109">Emellett minden értesítési hub-nak rendelkeznie kell hozzárendelt névtérrel.</span><span class="sxs-lookup"><span data-stu-id="72dfd-109">Additionally, all notification hubs must have an assigned namespace.</span></span>

<span data-ttu-id="72dfd-110">Ez a parancsmag elsősorban a névterek engedélyezéséhez és letiltásához használatos.</span><span class="sxs-lookup"><span data-stu-id="72dfd-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="72dfd-111">Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtérben lévő értesítési hubokhoz, és a rendszergazdák ezekkel a hubok segítségével küldhetnek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="72dfd-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="72dfd-112">Ha újra engedélyezni szeretné egy letiltott névtér használatát, ezzel a parancsmaggal állítsa be az aktív névtér **állapot** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="72dfd-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>

<span data-ttu-id="72dfd-113">Ezt a parancsmagot is megadhatja kritikusként a névtér címkézéséhez.</span><span class="sxs-lookup"><span data-stu-id="72dfd-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="72dfd-114">Ez a beállítás megakadályozza a névtér törlését.</span><span class="sxs-lookup"><span data-stu-id="72dfd-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="72dfd-115">A kritikus névterek eltávolításához előbb el kell távolítania a kritikus címkét.</span><span class="sxs-lookup"><span data-stu-id="72dfd-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="72dfd-116">Példák</span><span class="sxs-lookup"><span data-stu-id="72dfd-116">EXAMPLES</span></span>

### <span data-ttu-id="72dfd-117">Példa 1: névtér letiltása</span><span class="sxs-lookup"><span data-stu-id="72dfd-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="72dfd-118">Ez a parancs letiltja a ContosoPartners nevű névteret a West US Datacenter-ben, és a ContosoNotificationsGroup-erőforráscsoport számára van társítva.</span><span class="sxs-lookup"><span data-stu-id="72dfd-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="72dfd-119">2. példa: névtér engedélyezése</span><span class="sxs-lookup"><span data-stu-id="72dfd-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="72dfd-120">Ez a parancs lehetővé teszi, hogy a ContosoPartners nevű névtér a West US-adatközpontban található, és a ContosoNotificationsGroup erőforráscsoport legyen társítva.</span><span class="sxs-lookup"><span data-stu-id="72dfd-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="72dfd-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72dfd-121">PARAMETERS</span></span>

### <span data-ttu-id="72dfd-122">-Kritikus</span><span class="sxs-lookup"><span data-stu-id="72dfd-122">-Critical</span></span>
<span data-ttu-id="72dfd-123">Azt jelzi, hogy a névtér a kritikus névtér-e.</span><span class="sxs-lookup"><span data-stu-id="72dfd-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="72dfd-124">A kritikus névterek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="72dfd-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="72dfd-125">A kritikus névterek törléséhez a tulajdonság értékét false értékre kell állítania ahhoz, hogy a névteret nem kritikusként jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="72dfd-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="72dfd-126">-Force</span><span class="sxs-lookup"><span data-stu-id="72dfd-126">-Force</span></span>
<span data-ttu-id="72dfd-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72dfd-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="72dfd-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="72dfd-128">-Location</span></span>
<span data-ttu-id="72dfd-129">A névteret működtető adatközpont megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dfd-129">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="72dfd-130">Bár ezt a paramétert bármely érvényes Azure-helyre beállíthatja, így optimális teljesítményhez a felhasználók többségéhez közeli adatközpontot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="72dfd-130">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>

<span data-ttu-id="72dfd-131">Az Azure-helyek naprakész listáját az alábbi parancs futtatásával érheti el:</span><span class="sxs-lookup"><span data-stu-id="72dfd-131">To get an up-to-date list of Azure locations run the following command:</span></span>

`Get-AzureLocation | Select-Object DisplayName`

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

### <span data-ttu-id="72dfd-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72dfd-132">-Namespace</span></span>
<span data-ttu-id="72dfd-133">A parancsmag által módosított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dfd-133">Specifies the namespace that this cmdlet modifies.</span></span>

<span data-ttu-id="72dfd-134">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="72dfd-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="72dfd-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72dfd-135">-ResourceGroup</span></span>
<span data-ttu-id="72dfd-136">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="72dfd-136">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="72dfd-137">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="72dfd-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="72dfd-138">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="72dfd-138">-SkuTier</span></span>
<span data-ttu-id="72dfd-139">A névtér SKU-szintjei</span><span class="sxs-lookup"><span data-stu-id="72dfd-139">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="72dfd-140">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="72dfd-140">-State</span></span>
<span data-ttu-id="72dfd-141">A névtér aktuális állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dfd-141">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="72dfd-142">A paraméter elfogadható értékei a következők: aktív és le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="72dfd-142">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="72dfd-143">-Címkék</span><span class="sxs-lookup"><span data-stu-id="72dfd-143">-Tags</span></span>
<span data-ttu-id="72dfd-144">Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="72dfd-144">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="72dfd-145">A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.</span><span class="sxs-lookup"><span data-stu-id="72dfd-145">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="72dfd-146">Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.</span><span class="sxs-lookup"><span data-stu-id="72dfd-146">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="72dfd-147">Az egyéni címke két részből áll: a *név* és (tetszés szerint) az *érték*.</span><span class="sxs-lookup"><span data-stu-id="72dfd-147">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="72dfd-148">A részlegben például a címke neve részleg, a címke pedig az érték.</span><span class="sxs-lookup"><span data-stu-id="72dfd-148">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="72dfd-149">Címke hozzáadásához használja az alábbihoz hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016 címkét hozza létre:</span><span class="sxs-lookup"><span data-stu-id="72dfd-149">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

<span data-ttu-id="72dfd-150">-Címkéket @ {Name = "CalendarYear"; Value = "2016"}</span><span class="sxs-lookup"><span data-stu-id="72dfd-150">-Tags @{Name="CalendarYear";Value="2016"}</span></span>

<span data-ttu-id="72dfd-151">Ha több címkét szeretne felvenni ugyanabba a parancsba, vesszővel válassza el az egyes címkéket:</span><span class="sxs-lookup"><span data-stu-id="72dfd-151">To add multiple tags in the same command, separate the individual tags by using commas:</span></span>

<span data-ttu-id="72dfd-152">-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "pénzügyi év időszaka"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="72dfd-152">-Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="72dfd-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72dfd-153">-Confirm</span></span>
<span data-ttu-id="72dfd-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72dfd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dfd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dfd-155">-WhatIf</span></span>
<span data-ttu-id="72dfd-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72dfd-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72dfd-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72dfd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dfd-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dfd-158">-DefaultProfile</span></span>
<span data-ttu-id="72dfd-159">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72dfd-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72dfd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dfd-160">CommonParameters</span></span>
<span data-ttu-id="72dfd-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72dfd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dfd-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dfd-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dfd-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dfd-163">INPUTS</span></span>

## <span data-ttu-id="72dfd-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72dfd-164">OUTPUTS</span></span>

### <span data-ttu-id="72dfd-165">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="72dfd-165">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="72dfd-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72dfd-166">NOTES</span></span>

## <span data-ttu-id="72dfd-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72dfd-167">RELATED LINKS</span></span>

[<span data-ttu-id="72dfd-168">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72dfd-168">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="72dfd-169">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72dfd-169">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="72dfd-170">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72dfd-170">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


