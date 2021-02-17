---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158722"
---
# <span data-ttu-id="5bdf8-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5bdf8-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="5bdf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bdf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdf8-103">Beállítja egy értesítési központ névterének tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="5bdf8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bdf8-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdf8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bdf8-105">DESCRIPTION</span></span>
<span data-ttu-id="5bdf8-106">A **Set-AzNotificationHubsNamespace** parancsmag beállítja egy meglévő értesítési központ névterének tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="5bdf8-107">A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5bdf8-108">Legalább egy értesítési központ névterének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="5bdf8-109">Ezenkívül minden értesítési központhoz hozzá kell rendelni egy névteret.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="5bdf8-110">Ez a parancsmag elsősorban a névterek engedélyezésére és letiltására használható.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="5bdf8-111">Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtér egyik értesítési központjához sem, és a rendszergazdák sem tudnak leküldéses értesítéseket küldeni.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="5bdf8-112">Ha újra engedélyezni szeretné a letiltott névteret, ezzel a parancsmaggal állítsa a névtér **State** tulajdonságát Aktívra.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="5bdf8-113">Ez a parancsmag egy névteret is kritikusként címkézhet meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="5bdf8-114">Ez megakadályozza a névtér törlését.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="5bdf8-115">A kritikus névterek eltávolításához először el kell távolítania a kritikus címkét.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="5bdf8-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bdf8-116">EXAMPLES</span></span>

### <span data-ttu-id="5bdf8-117">1. példa: Névtér letiltása</span><span class="sxs-lookup"><span data-stu-id="5bdf8-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="5bdf8-118">Ez a parancs letiltja a ContosoPartners nevű névteret, amely az Amerikai Egyesült Államok nyugati részén található, és a ContosoNotificationsGroup erőforráscsoporthoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="5bdf8-119">2. példa: Névtér engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5bdf8-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="5bdf8-120">Ez a parancs engedélyezi a ContosoPartners nevű névteret, amely az Amerikai Egyesült Államok nyugati részén található, és a ContosoNotificationsGroup erőforráscsoporthoz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="5bdf8-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bdf8-121">PARAMETERS</span></span>

### <span data-ttu-id="5bdf8-122">-Critical</span><span class="sxs-lookup"><span data-stu-id="5bdf8-122">-Critical</span></span>
<span data-ttu-id="5bdf8-123">Azt jelzi, hogy a névtér kritikus névtér-e.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="5bdf8-124">A kritikus névterek nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="5bdf8-125">A kritikus névterek törléséhez a tulajdonság értékét Hamis értékre kell állítania ahhoz, hogy a névteret ne kritikusként jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="5bdf8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdf8-126">-DefaultProfile</span></span>
<span data-ttu-id="5bdf8-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bdf8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bdf8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="5bdf8-128">-Force</span></span>
<span data-ttu-id="5bdf8-129">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bdf8-130">-Location</span><span class="sxs-lookup"><span data-stu-id="5bdf8-130">-Location</span></span>
<span data-ttu-id="5bdf8-131">A névteret tartalmazó adatközpont megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="5bdf8-132">Bár ezt a paramétert bármilyen érvényes Azure-helyre beállíthatja, az optimális teljesítmény érdekében a legtöbb felhasználó közelében található adatközpontot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="5bdf8-133">Az Azure-helyek naprakész listájának lekértért futtatásához futtassa az alábbi parancsot: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="5bdf8-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="5bdf8-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5bdf8-134">-Namespace</span></span>
<span data-ttu-id="5bdf8-135">A parancsmag által módosítható névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="5bdf8-136">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5bdf8-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bdf8-137">-ResourceGroup</span></span>
<span data-ttu-id="5bdf8-138">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5bdf8-139">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5bdf8-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5bdf8-140">-SkuTier</span></span>
<span data-ttu-id="5bdf8-141">A névtér termékváltozatrétege</span><span class="sxs-lookup"><span data-stu-id="5bdf8-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="5bdf8-142">-State</span><span class="sxs-lookup"><span data-stu-id="5bdf8-142">-State</span></span>
<span data-ttu-id="5bdf8-143">A névtér aktuális állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="5bdf8-144">A paraméter elfogadható értékei: Aktív és Letiltva.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="5bdf8-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bdf8-145">-Tag</span></span>
<span data-ttu-id="5bdf8-146">Az Azure-elemek kategorizálására és rendezésére használható névérték-párokat ad meg.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="5bdf8-147">A címkék a kulcsszavakhoz hasonlóan működnek, és az egész telepítésben működnek.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="5bdf8-148">Ha például az összes olyan elemet megkeresi, amely a Department:IT címkével van megcímkézve, a keresés az adott címkével az összes Azure-elemet visszaadja, függetlenül az elem típusától, helyétől vagy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="5bdf8-149">Az egyes címkék két részből áll: a *Név* és (tetszés szerint) az *Érték.*</span><span class="sxs-lookup"><span data-stu-id="5bdf8-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="5bdf8-150">A Department:IT (Részleg) címke neve például Részleg, a címke értéke pedig IT.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="5bdf8-151">Címke hozzáadásához ehhez hasonló hash táblázatszintaxist használjon, amely létrehozza a CalendarYear:2016 címkét: -Tags @{Name="CalendarYear"; Value="2016"} Ha több címkét szeretne hozzáadni egy parancshoz, az egyes címkéket vesszővel válassza el egymástól: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="5bdf8-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="5bdf8-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bdf8-152">-Confirm</span></span>
<span data-ttu-id="5bdf8-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdf8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdf8-154">-WhatIf</span></span>
<span data-ttu-id="5bdf8-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bdf8-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdf8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdf8-157">CommonParameters</span></span>
<span data-ttu-id="5bdf8-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bdf8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdf8-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdf8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdf8-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bdf8-160">INPUTS</span></span>

### <span data-ttu-id="5bdf8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5bdf8-161">System.String</span></span>

### <span data-ttu-id="5bdf8-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="5bdf8-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="5bdf8-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bdf8-163">System.Boolean</span></span>

### <span data-ttu-id="5bdf8-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bdf8-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5bdf8-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bdf8-165">OUTPUTS</span></span>

### <span data-ttu-id="5bdf8-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5bdf8-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="5bdf8-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bdf8-167">NOTES</span></span>

## <span data-ttu-id="5bdf8-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bdf8-168">RELATED LINKS</span></span>

[<span data-ttu-id="5bdf8-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5bdf8-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5bdf8-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5bdf8-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5bdf8-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5bdf8-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


