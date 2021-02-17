---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158746"
---
# <span data-ttu-id="5fb66-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5fb66-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="5fb66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb66-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb66-103">Létrehoz egy értesítési központ névterét.</span><span class="sxs-lookup"><span data-stu-id="5fb66-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="5fb66-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fb66-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fb66-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fb66-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb66-106">A **New-AzNotificationHubsNamespace** parancsmag létrehoz egy értesítési központ névterét.</span><span class="sxs-lookup"><span data-stu-id="5fb66-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="5fb66-107">A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.</span><span class="sxs-lookup"><span data-stu-id="5fb66-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5fb66-108">Legalább egy értesítési központ névterének meg kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5fb66-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="5fb66-109">Egyetlen névterben több központ is elterhet.</span><span class="sxs-lookup"><span data-stu-id="5fb66-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="5fb66-110">Több névteret is adhat a központ rendszerezéséhez, vagy adott személyeknek engedélyt adhat a központok kijelölt alcsoportja kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="5fb66-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="5fb66-111">Névtér létrehozásához adjon meg egy egyedi nevet a névtérnek; adja meg azt az adatközpontot, ahol a névtér található; és adja meg azt az erőforráscsoportot, amelyhez a névteret hozzárendeli.</span><span class="sxs-lookup"><span data-stu-id="5fb66-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="5fb66-112">A névtér létrehozása után a New-AzNotificationHubsNamespaceAuthorizationRules parancsmag segítségével engedélyezési szabályokat rendelhet a névtérhez.</span><span class="sxs-lookup"><span data-stu-id="5fb66-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="5fb66-113">Az engedélyezési szabályok a névtér engedélyeinek kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="5fb66-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="5fb66-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fb66-114">EXAMPLES</span></span>

### <span data-ttu-id="5fb66-115">1. példa: Értesítési központ létrehozása</span><span class="sxs-lookup"><span data-stu-id="5fb66-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="5fb66-116">Ez a parancs létrehoz egy ContosoPartners nevű értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="5fb66-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="5fb66-117">A névtér a nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup erőforráscsoporthoz lesz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="5fb66-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="5fb66-118">2. példa: Értesítési központ létrehozása címkékkel</span><span class="sxs-lookup"><span data-stu-id="5fb66-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="5fb66-119">Ez a parancs létrehoz egy ContosoPartners nevű értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="5fb66-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="5fb66-120">A névtér a nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup erőforráscsoporthoz lesz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="5fb66-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="5fb66-121">Ez a parancs emellett létrehoz egy Címkét a Célközönség névvel és a PartnerOrganizations értékkel, és a névtérhez van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5fb66-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="5fb66-122">Ez biztosítja, hogy a névtér mindig megjelenik, amikor olyan elemekre szűr, amelyeknél a Célközönség címke partnerszervezetre van állítva.</span><span class="sxs-lookup"><span data-stu-id="5fb66-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="5fb66-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fb66-123">PARAMETERS</span></span>

### <span data-ttu-id="5fb66-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb66-124">-DefaultProfile</span></span>
<span data-ttu-id="5fb66-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fb66-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fb66-126">-Location</span><span class="sxs-lookup"><span data-stu-id="5fb66-126">-Location</span></span>
<span data-ttu-id="5fb66-127">A Névteret szolgáltató adatközpont megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb66-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="5fb66-128">Bár ezt a paramétert bármilyen érvényes helyre beállíthatja, az optimális teljesítmény érdekében érdemes lehet a felhasználók többségéhez közeli adatközpontot használni.</span><span class="sxs-lookup"><span data-stu-id="5fb66-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="5fb66-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb66-129">-Namespace</span></span>
<span data-ttu-id="5fb66-130">Az új névtér nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fb66-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="5fb66-131">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="5fb66-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5fb66-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fb66-132">-ResourceGroup</span></span>
<span data-ttu-id="5fb66-133">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="5fb66-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="5fb66-134">Az erőforráscsoportok olyan módon rendszerezhetik az elemeket, mint a névterek, az értesítési központok és az engedélyezési szabályok, ami egyszerű készletkezelést és felügyeletet kínál.</span><span class="sxs-lookup"><span data-stu-id="5fb66-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="5fb66-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5fb66-135">-SkuTier</span></span>
<span data-ttu-id="5fb66-136">A névtér termékváltozatrétege</span><span class="sxs-lookup"><span data-stu-id="5fb66-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="5fb66-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="5fb66-137">-Tag</span></span>
<span data-ttu-id="5fb66-138">Az Azure-elemek kategorizálásához és rendezéséhez használható névérték-párokat ad meg.</span><span class="sxs-lookup"><span data-stu-id="5fb66-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="5fb66-139">A címkék a kulcsszavakhoz hasonlóan működnek, és az egész telepítésben működnek.</span><span class="sxs-lookup"><span data-stu-id="5fb66-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="5fb66-140">Ha például az összes olyan elemet megkeresi, amely a Department:IT címkével van megcímkézve, a keresés az adott címkével az összes Azure-elemet visszaadja, függetlenül az elem típusától, helyétől vagy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="5fb66-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="5fb66-141">Az egyes címkék két részből áll: a *névből,* illetve szükség esetén az *Értékből.*</span><span class="sxs-lookup"><span data-stu-id="5fb66-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="5fb66-142">A Department:IT (Részleg) részlegnél például a címke neve Részleg, a címke értéke pedig IT.</span><span class="sxs-lookup"><span data-stu-id="5fb66-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="5fb66-143">Címke hozzáadásához ehhez hasonló hash táblázatszintaxist használjon, amely a CalendarYear:2016 címkét hozza létre:</span><span class="sxs-lookup"><span data-stu-id="5fb66-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="5fb66-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fb66-144">-Confirm</span></span>
<span data-ttu-id="5fb66-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5fb66-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb66-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb66-146">-WhatIf</span></span>
<span data-ttu-id="5fb66-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5fb66-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fb66-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fb66-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb66-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb66-149">CommonParameters</span></span>
<span data-ttu-id="5fb66-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb66-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb66-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb66-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb66-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fb66-152">INPUTS</span></span>

### <span data-ttu-id="5fb66-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5fb66-153">System.String</span></span>

### <span data-ttu-id="5fb66-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5fb66-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5fb66-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb66-155">OUTPUTS</span></span>

### <span data-ttu-id="5fb66-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5fb66-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="5fb66-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fb66-157">NOTES</span></span>

## <span data-ttu-id="5fb66-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fb66-158">RELATED LINKS</span></span>

[<span data-ttu-id="5fb66-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5fb66-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5fb66-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5fb66-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5fb66-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5fb66-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


