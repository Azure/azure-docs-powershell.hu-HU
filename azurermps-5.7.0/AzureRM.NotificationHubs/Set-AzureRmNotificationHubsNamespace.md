---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680684"
---
# <span data-ttu-id="cdef8-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cdef8-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="cdef8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdef8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdef8-103">Az értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdef8-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdef8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdef8-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdef8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdef8-105">DESCRIPTION</span></span>
<span data-ttu-id="cdef8-106">A **set-AzureRmNotificationHubsNamespace** parancsmag a meglévő értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdef8-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>

<span data-ttu-id="cdef8-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="cdef8-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="cdef8-108">Legalább egy értesítési hub-névtérnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="cdef8-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="cdef8-109">Emellett minden értesítési hub-nak rendelkeznie kell hozzárendelt névtérrel.</span><span class="sxs-lookup"><span data-stu-id="cdef8-109">Additionally, all notification hubs must have an assigned namespace.</span></span>

<span data-ttu-id="cdef8-110">Ez a parancsmag elsősorban a névterek engedélyezéséhez és letiltásához használatos.</span><span class="sxs-lookup"><span data-stu-id="cdef8-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="cdef8-111">Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtérben lévő értesítési hubokhoz, és a rendszergazdák ezekkel a hubok segítségével küldhetnek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="cdef8-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="cdef8-112">Ha újra engedélyezni szeretné egy letiltott névtér használatát, ezzel a parancsmaggal állítsa be az aktív névtér **állapot** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="cdef8-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>

<span data-ttu-id="cdef8-113">Ezt a parancsmagot is megadhatja kritikusként a névtér címkézéséhez.</span><span class="sxs-lookup"><span data-stu-id="cdef8-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="cdef8-114">Ez a beállítás megakadályozza a névtér törlését.</span><span class="sxs-lookup"><span data-stu-id="cdef8-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="cdef8-115">A kritikus névterek eltávolításához előbb el kell távolítania a kritikus címkét.</span><span class="sxs-lookup"><span data-stu-id="cdef8-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="cdef8-116">Példák</span><span class="sxs-lookup"><span data-stu-id="cdef8-116">EXAMPLES</span></span>

### <span data-ttu-id="cdef8-117">Példa 1: névtér letiltása</span><span class="sxs-lookup"><span data-stu-id="cdef8-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="cdef8-118">Ez a parancs letiltja a ContosoPartners nevű névteret a West US Datacenter-ben, és a ContosoNotificationsGroup-erőforráscsoport számára van társítva.</span><span class="sxs-lookup"><span data-stu-id="cdef8-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="cdef8-119">2. példa: névtér engedélyezése</span><span class="sxs-lookup"><span data-stu-id="cdef8-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="cdef8-120">Ez a parancs lehetővé teszi, hogy a ContosoPartners nevű névtér a West US-adatközpontban található, és a ContosoNotificationsGroup erőforráscsoport legyen társítva.</span><span class="sxs-lookup"><span data-stu-id="cdef8-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="cdef8-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdef8-121">PARAMETERS</span></span>

### <span data-ttu-id="cdef8-122">-Kritikus</span><span class="sxs-lookup"><span data-stu-id="cdef8-122">-Critical</span></span>
<span data-ttu-id="cdef8-123">Azt jelzi, hogy a névtér a kritikus névtér-e.</span><span class="sxs-lookup"><span data-stu-id="cdef8-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="cdef8-124">A kritikus névterek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="cdef8-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="cdef8-125">A kritikus névterek törléséhez a tulajdonság értékét false értékre kell állítania ahhoz, hogy a névteret nem kritikusként jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="cdef8-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdef8-126">-DefaultProfile</span></span>
<span data-ttu-id="cdef8-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cdef8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdef8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="cdef8-128">-Force</span></span>
<span data-ttu-id="cdef8-129">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdef8-129">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cdef8-130">-Location</span></span>
<span data-ttu-id="cdef8-131">A névteret működtető adatközpont megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdef8-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="cdef8-132">Bár ezt a paramétert bármely érvényes Azure-helyre beállíthatja, így optimális teljesítményhez a felhasználók többségéhez közeli adatközpontot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="cdef8-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>

<span data-ttu-id="cdef8-133">Az Azure-helyek naprakész listáját az alábbi parancs futtatásával érheti el:</span><span class="sxs-lookup"><span data-stu-id="cdef8-133">To get an up-to-date list of Azure locations run the following command:</span></span>

`Get-AzureLocation | Select-Object DisplayName`

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

### <span data-ttu-id="cdef8-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdef8-134">-Namespace</span></span>
<span data-ttu-id="cdef8-135">A parancsmag által módosított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdef8-135">Specifies the namespace that this cmdlet modifies.</span></span>

<span data-ttu-id="cdef8-136">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="cdef8-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cdef8-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdef8-137">-ResourceGroup</span></span>
<span data-ttu-id="cdef8-138">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="cdef8-138">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="cdef8-139">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="cdef8-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cdef8-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cdef8-140">-SkuTier</span></span>
<span data-ttu-id="cdef8-141">A névtér SKU-szintjei</span><span class="sxs-lookup"><span data-stu-id="cdef8-141">Sku tier of the namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-142">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="cdef8-142">-State</span></span>
<span data-ttu-id="cdef8-143">A névtér aktuális állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdef8-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="cdef8-144">A paraméter elfogadható értékei a következők: aktív és le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="cdef8-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="cdef8-145">-Tag</span></span>
<span data-ttu-id="cdef8-146">Az Azure-elemek kategorizálására és rendszerezésére használható név-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdef8-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="cdef8-147">A címkék a kulcsszavakhoz hasonlóan működnek, és a központi üzembe állítások között működnek.</span><span class="sxs-lookup"><span data-stu-id="cdef8-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="cdef8-148">Ha például az összes elemet megkeresi a címke részleggel: a keresés a címkét tartalmazó összes Azure-elemet visszaadja, függetlenül az elemtípus, a hely vagy az erőforráscsoport nevétől.</span><span class="sxs-lookup"><span data-stu-id="cdef8-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="cdef8-149">Az egyéni címke két részből áll: a *név* és (tetszés szerint) az *érték*.</span><span class="sxs-lookup"><span data-stu-id="cdef8-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="cdef8-150">A részlegben például a címke neve részleg, a címke pedig az érték.</span><span class="sxs-lookup"><span data-stu-id="cdef8-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="cdef8-151">Címke hozzáadásához használja az alábbihoz hasonló hash-táblázat szintaxisát, amely a CalendarYear: 2016 címkét hozza létre:</span><span class="sxs-lookup"><span data-stu-id="cdef8-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

<span data-ttu-id="cdef8-152">-Címkéket @ {Name = "CalendarYear"; Value = "2016"}</span><span class="sxs-lookup"><span data-stu-id="cdef8-152">-Tags @{Name="CalendarYear";Value="2016"}</span></span>

<span data-ttu-id="cdef8-153">Ha több címkét szeretne felvenni ugyanabba a parancsba, vesszővel válassza el az egyes címkéket:</span><span class="sxs-lookup"><span data-stu-id="cdef8-153">To add multiple tags in the same command, separate the individual tags by using commas:</span></span>

<span data-ttu-id="cdef8-154">-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "pénzügyi év időszaka"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="cdef8-154">-Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdef8-155">-Confirm</span></span>
<span data-ttu-id="cdef8-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdef8-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdef8-157">-WhatIf</span></span>
<span data-ttu-id="cdef8-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdef8-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdef8-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdef8-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdef8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdef8-160">CommonParameters</span></span>
<span data-ttu-id="cdef8-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdef8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdef8-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdef8-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdef8-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdef8-163">INPUTS</span></span>

### <span data-ttu-id="cdef8-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="cdef8-164">None</span></span>
<span data-ttu-id="cdef8-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cdef8-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdef8-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdef8-166">OUTPUTS</span></span>

### <span data-ttu-id="cdef8-167">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cdef8-167">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="cdef8-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdef8-168">NOTES</span></span>

## <span data-ttu-id="cdef8-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdef8-169">RELATED LINKS</span></span>

[<span data-ttu-id="cdef8-170">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cdef8-170">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="cdef8-171">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cdef8-171">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="cdef8-172">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cdef8-172">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


