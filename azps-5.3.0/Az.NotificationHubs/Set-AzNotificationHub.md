---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385067"
---
# <span data-ttu-id="cc756-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc756-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="cc756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc756-102">SYNOPSIS</span></span>
<span data-ttu-id="cc756-103">Egy értesítési központ tulajdonságértékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc756-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="cc756-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc756-104">SYNTAX</span></span>

### <span data-ttu-id="cc756-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc756-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc756-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc756-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc756-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc756-107">DESCRIPTION</span></span>
<span data-ttu-id="cc756-108">A **Set-AzNotificationHub** parancsmag módosítja egy értesítési központ tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="cc756-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="cc756-109">Az értesítési központ tulajdonságértékét kétféleképpen módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="cc756-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="cc756-110">Az egyik esetben létrehozhatja a **NotificationHubAttributes** objektum egy példányát, majd beállíthatja az objektumot a tulajdonságértékekkel, amelyekhez az új központnak rendelkeznie kell.</span><span class="sxs-lookup"><span data-stu-id="cc756-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="cc756-111">Ezt a .NET-keretrendszeren keresztül lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="cc756-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="cc756-112">Ezután az *NotificationHubObj* paraméterrel átmásolhatja ezeket a tulajdonságértékeket a központba.</span><span class="sxs-lookup"><span data-stu-id="cc756-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="cc756-113">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a vonatkozó konfigurációs értékeket, majd az *InputFile* paraméterrel alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="cc756-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="cc756-114">A JSON-fájl olyan szövegfájl, amely a következő szintaxist használja: {</span><span class="sxs-lookup"><span data-stu-id="cc756-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="cc756-115">"Név": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="cc756-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="cc756-116">"Hely": "Nyugat-USA",</span><span class="sxs-lookup"><span data-stu-id="cc756-116">"Location": "West US",</span></span>  
<span data-ttu-id="cc756-117">} A **Set-AzNotificationHub** parancsmaggal együtt használva az előző JSON-minta beállítja egy ContosoNotificationHub nevű értesítési központ helyértékét az Egyesült Államok nyugati részén.</span><span class="sxs-lookup"><span data-stu-id="cc756-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="cc756-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc756-118">EXAMPLES</span></span>

### <span data-ttu-id="cc756-119">1. példa: Az értesítési központ tulajdonságértékének módosítása</span><span class="sxs-lookup"><span data-stu-id="cc756-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="cc756-120">Ez a parancs módosítja a ContosoNamespace névterében található értesítési központ tulajdonságértékét, és hozzárendeli azt a ContosoNotificationsGroup erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="cc756-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="cc756-121">A tulajdonságértékek, valamint a módosítandó központ neve nincs megadva a parancsban.</span><span class="sxs-lookup"><span data-stu-id="cc756-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="cc756-122">Ehelyett ez az információ a bemeneti fájlban C:\Configuration\Hubs.jsbe van stb.</span><span class="sxs-lookup"><span data-stu-id="cc756-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="cc756-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="cc756-123">Example 2</span></span>

<span data-ttu-id="cc756-124">Egy értesítési központ tulajdonságértékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="cc756-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="cc756-125">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="cc756-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="cc756-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc756-126">PARAMETERS</span></span>

### <span data-ttu-id="cc756-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc756-127">-DefaultProfile</span></span>
<span data-ttu-id="cc756-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cc756-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc756-129">-Force</span><span class="sxs-lookup"><span data-stu-id="cc756-129">-Force</span></span>
<span data-ttu-id="cc756-130">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc756-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc756-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cc756-131">-InputFile</span></span>
<span data-ttu-id="cc756-132">Az értesítési központ konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc756-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="cc756-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc756-133">-Namespace</span></span>
<span data-ttu-id="cc756-134">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cc756-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="cc756-135">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="cc756-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cc756-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="cc756-136">-NotificationHubObj</span></span>
<span data-ttu-id="cc756-137">Megadja a **NotificationHubAttributes** objektumot, amely a parancsmag által módosított központ konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cc756-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc756-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc756-138">-ResourceGroup</span></span>
<span data-ttu-id="cc756-139">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cc756-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="cc756-140">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="cc756-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cc756-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc756-141">-Confirm</span></span>
<span data-ttu-id="cc756-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc756-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc756-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc756-143">-WhatIf</span></span>
<span data-ttu-id="cc756-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc756-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc756-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc756-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc756-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc756-146">CommonParameters</span></span>
<span data-ttu-id="cc756-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc756-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc756-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc756-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc756-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc756-149">INPUTS</span></span>

### <span data-ttu-id="cc756-150">System.String</span><span class="sxs-lookup"><span data-stu-id="cc756-150">System.String</span></span>

## <span data-ttu-id="cc756-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc756-151">OUTPUTS</span></span>

### <span data-ttu-id="cc756-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="cc756-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="cc756-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc756-153">NOTES</span></span>

## <span data-ttu-id="cc756-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc756-154">RELATED LINKS</span></span>

[<span data-ttu-id="cc756-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc756-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="cc756-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc756-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="cc756-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc756-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


