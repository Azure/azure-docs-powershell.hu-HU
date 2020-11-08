---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 3dc4a81731f42ce6a27ae5d23fb7c81af76cf789
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024526"
---
# <span data-ttu-id="53b58-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="53b58-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="53b58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53b58-102">SYNOPSIS</span></span>
<span data-ttu-id="53b58-103">Egy értesítési központhoz tartozó tulajdonságértékek beállítása.</span><span class="sxs-lookup"><span data-stu-id="53b58-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="53b58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53b58-104">SYNTAX</span></span>

### <span data-ttu-id="53b58-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b58-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b58-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b58-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53b58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53b58-107">DESCRIPTION</span></span>
<span data-ttu-id="53b58-108">A **set-AzNotificationHub** parancsmag módosította egy értesítési hub tulajdonság értékét.</span><span class="sxs-lookup"><span data-stu-id="53b58-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="53b58-109">Az értesítési hub tulajdonság értékét két módon módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="53b58-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="53b58-110">Ehhez létre kell hoznia egy példányt a **NotificationHubAttributes** objektumból, majd konfigurálnia kell az objektumot azzal az értékkel, amelyet az új hub-nak meg szeretne jeleníteni.</span><span class="sxs-lookup"><span data-stu-id="53b58-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="53b58-111">Ez a .NET-keretrendszeren keresztül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="53b58-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="53b58-112">Ezt követően a *NotificationHubObj* paraméterrel átmásolhatja az adott tulajdonság értékét a központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="53b58-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="53b58-113">Azt is megteheti, hogy létrehoz egy JSON-fájlt (JavaScript-objektum jelölését), amely tartalmazza a megfelelő konfigurációs értékeket, majd ezeket az értékeket a *InputFile* paraméterrel alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="53b58-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="53b58-114">A JSON-fájl egy szöveges fájl, amely a következőhöz hasonló szintaxist használ: {</span><span class="sxs-lookup"><span data-stu-id="53b58-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="53b58-115">"Név": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="53b58-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="53b58-116">"Hely": "Nyugat-amerikai",</span><span class="sxs-lookup"><span data-stu-id="53b58-116">"Location": "West US",</span></span>  
<span data-ttu-id="53b58-117">} Ha a **set-AzNotificationHub** parancsmaggal együtt használja, az előző JSON-minta a ContosoNotificationHub nevű értesítési központ helyének értékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="53b58-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="53b58-118">Példák</span><span class="sxs-lookup"><span data-stu-id="53b58-118">EXAMPLES</span></span>

### <span data-ttu-id="53b58-119">Példa 1: az értesítési központ tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="53b58-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="53b58-120">Ez a parancs módosítja a ContosoNamespace névtérben talált értesítési központ tulajdonságának értékeit, és hozzárendelte azt az erőforráscsoport ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="53b58-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="53b58-121">A tulajdonság értéke, valamint a módosítandó hub neve nincs megadva a parancsban.</span><span class="sxs-lookup"><span data-stu-id="53b58-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="53b58-122">Ehelyett ezek az információk a bemeneti fájlban C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="53b58-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="53b58-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53b58-123">PARAMETERS</span></span>

### <span data-ttu-id="53b58-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b58-124">-DefaultProfile</span></span>
<span data-ttu-id="53b58-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53b58-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53b58-126">-Force</span><span class="sxs-lookup"><span data-stu-id="53b58-126">-Force</span></span>
<span data-ttu-id="53b58-127">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53b58-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="53b58-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="53b58-128">-InputFile</span></span>
<span data-ttu-id="53b58-129">Az értesítési központ konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53b58-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="53b58-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="53b58-130">-Namespace</span></span>
<span data-ttu-id="53b58-131">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="53b58-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="53b58-132">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="53b58-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="53b58-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="53b58-133">-NotificationHubObj</span></span>
<span data-ttu-id="53b58-134">Azt a **NotificationHubAttributes** -objektumot adja meg, amely a parancsmag által módosított hub konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="53b58-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="53b58-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53b58-135">-ResourceGroup</span></span>
<span data-ttu-id="53b58-136">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="53b58-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="53b58-137">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="53b58-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="53b58-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53b58-138">-Confirm</span></span>
<span data-ttu-id="53b58-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53b58-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b58-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b58-140">-WhatIf</span></span>
<span data-ttu-id="53b58-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53b58-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53b58-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53b58-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b58-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b58-143">CommonParameters</span></span>
<span data-ttu-id="53b58-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53b58-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b58-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b58-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b58-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53b58-146">INPUTS</span></span>

### <span data-ttu-id="53b58-147">System. String</span><span class="sxs-lookup"><span data-stu-id="53b58-147">System.String</span></span>

## <span data-ttu-id="53b58-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53b58-148">OUTPUTS</span></span>

### <span data-ttu-id="53b58-149">Microsoft. Azure. Command. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="53b58-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="53b58-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53b58-150">NOTES</span></span>

## <span data-ttu-id="53b58-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53b58-151">RELATED LINKS</span></span>

[<span data-ttu-id="53b58-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="53b58-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="53b58-153">Új – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="53b58-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="53b58-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="53b58-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


