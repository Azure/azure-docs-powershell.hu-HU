---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918177"
---
# <span data-ttu-id="4a5db-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a5db-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="4a5db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a5db-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5db-103">Egy értesítési központ tulajdonságértékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="4a5db-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="4a5db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a5db-104">SYNTAX</span></span>

### <span data-ttu-id="4a5db-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a5db-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a5db-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a5db-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a5db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a5db-107">DESCRIPTION</span></span>
<span data-ttu-id="4a5db-108">A **Set-AzNotificationHub** parancsmag módosítja egy értesítési központ tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="4a5db-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="4a5db-109">Az értesítési központ tulajdonságértékét kétféleképpen módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="4a5db-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="4a5db-110">Az egyik esetben létrehozhatja a **NotificationHubAttributes** objektum egy példányát, majd beállíthatja az objektumot a tulajdonságértékekkel, amelyekhez az új központnak rendelkeznie kell.</span><span class="sxs-lookup"><span data-stu-id="4a5db-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="4a5db-111">Ezt a .NET-keretrendszeren keresztül lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="4a5db-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="4a5db-112">Ezután az *NotificationHubObj* paraméterrel átmásolhatja ezeket a tulajdonságértékeket a központba.</span><span class="sxs-lookup"><span data-stu-id="4a5db-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="4a5db-113">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a megfelelő konfigurációs értékeket, majd az *InputFile* paraméterrel alkalmazza ezeket az értékeket.</span><span class="sxs-lookup"><span data-stu-id="4a5db-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="4a5db-114">A JSON-fájl olyan szövegfájl, amely a következő szintaxist használja: {</span><span class="sxs-lookup"><span data-stu-id="4a5db-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="4a5db-115">"Név": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="4a5db-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="4a5db-116">"Hely": "Nyugat-USA",</span><span class="sxs-lookup"><span data-stu-id="4a5db-116">"Location": "West US",</span></span>  
<span data-ttu-id="4a5db-117">} Ha a **Set-AzNotificationHub** parancsmaggal együtt használja, az előző JSON-minta beállítja a ContosoNotificationHub nevű értesítési központ Hely értékét az Egyesült Államok nyugati felére.</span><span class="sxs-lookup"><span data-stu-id="4a5db-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="4a5db-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a5db-118">EXAMPLES</span></span>

### <span data-ttu-id="4a5db-119">1. példa: Az értesítési központ tulajdonságértékének módosítása</span><span class="sxs-lookup"><span data-stu-id="4a5db-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="4a5db-120">Ez a parancs módosítja a ContosoNamespace névterében található értesítési központ tulajdonságértékét, és hozzárendeli azt a ContosoNotificationsGroup erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4a5db-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="4a5db-121">A tulajdonságértékek, valamint a módosítandó központ neve nincs megadva a parancsban.</span><span class="sxs-lookup"><span data-stu-id="4a5db-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="4a5db-122">Ehelyett ez az információ a bemeneti fájlban C:\Configuration\Hubs.jsbe van stb.</span><span class="sxs-lookup"><span data-stu-id="4a5db-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="4a5db-123">2. példa</span><span class="sxs-lookup"><span data-stu-id="4a5db-123">Example 2</span></span>

<span data-ttu-id="4a5db-124">Egy értesítési központ tulajdonságértékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="4a5db-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="4a5db-125">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="4a5db-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="4a5db-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a5db-126">PARAMETERS</span></span>

### <span data-ttu-id="4a5db-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5db-127">-DefaultProfile</span></span>
<span data-ttu-id="4a5db-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4a5db-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a5db-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4a5db-129">-Force</span></span>
<span data-ttu-id="4a5db-130">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a5db-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a5db-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4a5db-131">-InputFile</span></span>
<span data-ttu-id="4a5db-132">Az értesítési központ konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a5db-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="4a5db-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a5db-133">-Namespace</span></span>
<span data-ttu-id="4a5db-134">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4a5db-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4a5db-135">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="4a5db-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4a5db-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="4a5db-136">-NotificationHubObj</span></span>
<span data-ttu-id="4a5db-137">Megadja a **NotificationHubAttributes** objektumot, amely a parancsmag által módosított központ konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4a5db-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4a5db-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a5db-138">-ResourceGroup</span></span>
<span data-ttu-id="4a5db-139">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4a5db-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4a5db-140">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="4a5db-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4a5db-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a5db-141">-Confirm</span></span>
<span data-ttu-id="4a5db-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4a5db-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5db-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5db-143">-WhatIf</span></span>
<span data-ttu-id="4a5db-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4a5db-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a5db-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a5db-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5db-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5db-146">CommonParameters</span></span>
<span data-ttu-id="4a5db-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a5db-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5db-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5db-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5db-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a5db-149">INPUTS</span></span>

### <span data-ttu-id="4a5db-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4a5db-150">System.String</span></span>

## <span data-ttu-id="4a5db-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a5db-151">OUTPUTS</span></span>

### <span data-ttu-id="4a5db-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4a5db-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="4a5db-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a5db-153">NOTES</span></span>

## <span data-ttu-id="4a5db-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a5db-154">RELATED LINKS</span></span>

[<span data-ttu-id="4a5db-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a5db-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="4a5db-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a5db-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="4a5db-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a5db-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


