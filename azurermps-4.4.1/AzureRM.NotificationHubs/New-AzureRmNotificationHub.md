---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493401"
---
# <span data-ttu-id="2f582-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2f582-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="2f582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f582-102">SYNOPSIS</span></span>
<span data-ttu-id="2f582-103">Értesítési hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2f582-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f582-104">SYNTAX</span></span>

### <span data-ttu-id="2f582-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f582-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f582-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f582-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f582-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f582-107">DESCRIPTION</span></span>
<span data-ttu-id="2f582-108">A **New-AzureRmNotificationHub** parancsmag létrehoz egy értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="2f582-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="2f582-109">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="2f582-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="2f582-110">Az értesítési hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="2f582-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="2f582-111">A **New-AzureRmNotificationHub** parancsmag kétféle módon hozhat létre új értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="2f582-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="2f582-112">A **NotificationHubAttributes** objektum példányát létrehozhatja, majd beállíthatja az objektum beállítását.</span><span class="sxs-lookup"><span data-stu-id="2f582-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="2f582-113">Ezt követően a *NotificationHubObj* paraméterrel átmásolhatja az adott tulajdonság értékét az új központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="2f582-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="2f582-114">Azt is megteheti, hogy a megfelelő konfigurációs értékeket tartalmazó JSON (JavaScript-objektum jelölése) fájlt hoz létre, majd a *InputFile* paraméterrel alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="2f582-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="2f582-115">Ha a **New-AzureRmNotificationHub** parancsmaggal együtt használja, az előző JSON-minta létrehoz egy ContosoNotificationHub nevű, a West US Datacenter nevű nevű értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="2f582-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="2f582-116">Példák</span><span class="sxs-lookup"><span data-stu-id="2f582-116">EXAMPLES</span></span>

### <span data-ttu-id="2f582-117">Példa 1: értesítési központ létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f582-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="2f582-118">A parancs létrehoz egy értesítési hubot a névtér ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="2f582-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="2f582-119">Az új hubot a program hozzárendeli a ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="2f582-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="2f582-120">Nem kell megadnia egy nevet vagy a hub egyéb konfigurációs adatait; ezt az információt a program a bemeneti fájlból C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="2f582-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="2f582-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f582-121">PARAMETERS</span></span>

### <span data-ttu-id="2f582-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2f582-122">-InputFile</span></span>
<span data-ttu-id="2f582-123">Az új értesítési központ konfigurációs értékeit tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f582-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f582-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f582-124">-Namespace</span></span>
<span data-ttu-id="2f582-125">Azt a névteret adja meg, amelyhez az értesítési hub hozzá lesz rendelve.</span><span class="sxs-lookup"><span data-stu-id="2f582-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="2f582-126">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="2f582-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="2f582-127">Az értesítési hubokat egy meglévő névtérhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="2f582-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="2f582-128">A **New-AzureRmNotificationHub** parancsmag nem tud új névteret létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2f582-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="2f582-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="2f582-129">-NotificationHubObj</span></span>
<span data-ttu-id="2f582-130">Azt a **NotificationHubAttributes** -objektumot adja meg, amely az új hub konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2f582-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f582-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2f582-131">-ResourceGroup</span></span>
<span data-ttu-id="2f582-132">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá lesz rendelve.</span><span class="sxs-lookup"><span data-stu-id="2f582-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="2f582-133">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="2f582-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="2f582-134">Egy meglévő erőforráscsoportot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="2f582-134">You must use an existing resource group.</span></span>
<span data-ttu-id="2f582-135">A **New-AzureRmNotificationHub** parancsmag nem tud új erőforráscsoportot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2f582-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="2f582-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f582-136">-Confirm</span></span>
<span data-ttu-id="2f582-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f582-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f582-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f582-138">-WhatIf</span></span>
<span data-ttu-id="2f582-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f582-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f582-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f582-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f582-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f582-141">-DefaultProfile</span></span>
<span data-ttu-id="2f582-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f582-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f582-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f582-143">CommonParameters</span></span>
<span data-ttu-id="2f582-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f582-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f582-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f582-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f582-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f582-146">INPUTS</span></span>

## <span data-ttu-id="2f582-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f582-147">OUTPUTS</span></span>

### <span data-ttu-id="2f582-148">Microsoft. Azure. Command. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2f582-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="2f582-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f582-149">NOTES</span></span>

## <span data-ttu-id="2f582-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f582-150">RELATED LINKS</span></span>

[<span data-ttu-id="2f582-151">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2f582-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="2f582-152">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2f582-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="2f582-153">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2f582-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


