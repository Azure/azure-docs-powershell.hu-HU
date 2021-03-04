---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918258"
---
# <span data-ttu-id="614e4-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="614e4-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="614e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614e4-102">SYNOPSIS</span></span>
<span data-ttu-id="614e4-103">Létrehoz egy értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="614e4-103">Creates a notification hub.</span></span>

## <span data-ttu-id="614e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="614e4-104">SYNTAX</span></span>

### <span data-ttu-id="614e4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="614e4-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="614e4-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="614e4-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="614e4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="614e4-107">DESCRIPTION</span></span>
<span data-ttu-id="614e4-108">A **New-AzNotificationHub** parancsmag létrehoz egy értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="614e4-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="614e4-109">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="614e4-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="614e4-110">Az értesítési központok nagyjából egyenértékűek az egyes appokkal: mindegyik alkalmazásnak általában saját értesítési központja lesz.</span><span class="sxs-lookup"><span data-stu-id="614e4-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="614e4-111">A **New-AzNotificationHub** parancsmag kétféleképpen hozhat létre új értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="614e4-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="614e4-112">Létrehozhatja az **NotificationHubAttributes** objektum egy példányát, majd beállíthatja azt.</span><span class="sxs-lookup"><span data-stu-id="614e4-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="614e4-113">Ezután az *NotificationHubObj* paraméterrel átmásolhatja ezeket a tulajdonságértékeket az új központba.</span><span class="sxs-lookup"><span data-stu-id="614e4-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="614e4-114">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a vonatkozó konfigurációs értékeket, majd az *InputFile* paraméter használatával alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="614e4-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="614e4-115">A **New-AzNotificationHub** parancsmaggal együtt használva az előző JSON-minta létrehoz egy ContosoNotificationHub nevű értesítési központot az EGYESÜLT ÁLLAMOK nyugati részén található adatközpontban.</span><span class="sxs-lookup"><span data-stu-id="614e4-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="614e4-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="614e4-116">EXAMPLES</span></span>

### <span data-ttu-id="614e4-117">1. példa: Értesítési központ létrehozása</span><span class="sxs-lookup"><span data-stu-id="614e4-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="614e4-118">Ez a parancs létrehoz egy értesítési központot a ContosoNamespace névterében.</span><span class="sxs-lookup"><span data-stu-id="614e4-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="614e4-119">Az új központ hozzá lesz rendelve a ContosoNotificationsGroup csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="614e4-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="614e4-120">Nem kell megadnia a központ nevét vagy egyéb konfigurációs adatait; adatokat a rendszer a bemeneti fájlból fogja C:\Configurations\InternalHub.jsbe.</span><span class="sxs-lookup"><span data-stu-id="614e4-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="614e4-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="614e4-121">PARAMETERS</span></span>

### <span data-ttu-id="614e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614e4-122">-DefaultProfile</span></span>
<span data-ttu-id="614e4-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="614e4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="614e4-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="614e4-124">-InputFile</span></span>
<span data-ttu-id="614e4-125">Az új értesítési központ konfigurációs értékeit tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="614e4-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="614e4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="614e4-126">-Namespace</span></span>
<span data-ttu-id="614e4-127">Azt a névteret adja meg, amelyhez az értesítési központot hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="614e4-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="614e4-128">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="614e4-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="614e4-129">Az értesítési központokat hozzá kell rendelni egy meglévő névtérhez.</span><span class="sxs-lookup"><span data-stu-id="614e4-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="614e4-130">A **New-AzNotificationHub** parancsmag nem tud új névteret létrehozni.</span><span class="sxs-lookup"><span data-stu-id="614e4-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="614e4-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="614e4-131">-NotificationHubObj</span></span>
<span data-ttu-id="614e4-132">Az új központ konfigurációs adatait tartalmazó **NotificationHubAttributes** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="614e4-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="614e4-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="614e4-133">-ResourceGroup</span></span>
<span data-ttu-id="614e4-134">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központot hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="614e4-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="614e4-135">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="614e4-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="614e4-136">Meglévő erőforráscsoportot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="614e4-136">You must use an existing resource group.</span></span>
<span data-ttu-id="614e4-137">A **New-AzNotificationHub** parancsmag nem tud új erőforráscsoportot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="614e4-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="614e4-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="614e4-138">-Confirm</span></span>
<span data-ttu-id="614e4-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="614e4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="614e4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614e4-140">-WhatIf</span></span>
<span data-ttu-id="614e4-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="614e4-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="614e4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="614e4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="614e4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614e4-143">CommonParameters</span></span>
<span data-ttu-id="614e4-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614e4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614e4-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614e4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614e4-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="614e4-146">INPUTS</span></span>

### <span data-ttu-id="614e4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="614e4-147">System.String</span></span>

## <span data-ttu-id="614e4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="614e4-148">OUTPUTS</span></span>

### <span data-ttu-id="614e4-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="614e4-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="614e4-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="614e4-150">NOTES</span></span>

## <span data-ttu-id="614e4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="614e4-151">RELATED LINKS</span></span>

[<span data-ttu-id="614e4-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="614e4-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="614e4-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="614e4-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="614e4-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="614e4-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


