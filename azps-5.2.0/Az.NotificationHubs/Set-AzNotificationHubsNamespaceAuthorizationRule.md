---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336113"
---
# <span data-ttu-id="36d4e-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36d4e-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="36d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="36d4e-103">Engedélyezési szabályokat állít be az értesítési központ névterében.</span><span class="sxs-lookup"><span data-stu-id="36d4e-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="36d4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36d4e-104">SYNTAX</span></span>

### <span data-ttu-id="36d4e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d4e-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36d4e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d4e-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d4e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36d4e-107">DESCRIPTION</span></span>
<span data-ttu-id="36d4e-108">A **Set-AzNotificationHubsNamespaceAuthorizationRule** parancsmag módosítja az értesítési központ névterhez rendelt Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="36d4e-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="36d4e-109">Az engedélyezési szabályok kezelik a névtér és a névtérben található értesítési központok felhasználói jogait.</span><span class="sxs-lookup"><span data-stu-id="36d4e-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="36d4e-110">Ez a parancsmag két módszert biztosít a névtérhez rendelt engedélyezési szabály módosítására.</span><span class="sxs-lookup"><span data-stu-id="36d4e-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="36d4e-111">Az egyik esetben létrehozhatja a **SharedAccessAuthorizationRuleAttributes** objektum egy példányát, majd beállíthatja az objektumot a szabály birtokában található tulajdonságértékekkel.</span><span class="sxs-lookup"><span data-stu-id="36d4e-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="36d4e-112">Ehhez használhatja a .NET-keretrendszert.</span><span class="sxs-lookup"><span data-stu-id="36d4e-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="36d4e-113">Ezután ezeket a tulajdonságértékeket átmásolhatja a szabályba az *SASRule paraméteren* keresztül.</span><span class="sxs-lookup"><span data-stu-id="36d4e-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="36d4e-114">Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a megfelelő konfigurációs értékeket, majd alkalmazza ezeket az értékeket az *InputFile paraméteren* keresztül.</span><span class="sxs-lookup"><span data-stu-id="36d4e-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="36d4e-115">A JSON-fájl a következő szintaxishoz hasonló szintaxist használó szövegfájl: {</span><span class="sxs-lookup"><span data-stu-id="36d4e-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="36d4e-116">"Név": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="36d4e-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="36d4e-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="36d4e-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="36d4e-118">"Jogok": \[</span><span class="sxs-lookup"><span data-stu-id="36d4e-118">"Rights": \[</span></span>  
        <span data-ttu-id="36d4e-119">"Figyel",</span><span class="sxs-lookup"><span data-stu-id="36d4e-119">"Listen",</span></span>  
        <span data-ttu-id="36d4e-120">"Küldés"</span><span class="sxs-lookup"><span data-stu-id="36d4e-120">"Send"</span></span>  
    \]  
<span data-ttu-id="36d4e-121">} Ha a **Set-AzNotificationHubsNamespaceAuthorizationRule** parancsmaggal együtt használja, az előző JSON-minta módosítja a ContosoAuthorizationRule engedélyezési szabályt, hogy a felhasználók figyelési és küldési jogokat adjanak a névtérnek.</span><span class="sxs-lookup"><span data-stu-id="36d4e-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="36d4e-122">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36d4e-122">EXAMPLES</span></span>

### <span data-ttu-id="36d4e-123">1. példa: A névtérhez rendelt engedélyezési szabály módosítása</span><span class="sxs-lookup"><span data-stu-id="36d4e-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="36d4e-124">Ez a parancs módosítja a ContosoNamespace nevű névtérhez rendelt engedélyezési szabályt.</span><span class="sxs-lookup"><span data-stu-id="36d4e-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="36d4e-125">Meg kell adnia azt az erőforráscsoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="36d4e-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="36d4e-126">Az engedélyezési szabályra vonatkozó információk nem szerepelnek magában a parancsban.</span><span class="sxs-lookup"><span data-stu-id="36d4e-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="36d4e-127">Ehelyett ezt az információt a bemeneti fájlból C:\Configuration\AuthorizationRules.jsbe.</span><span class="sxs-lookup"><span data-stu-id="36d4e-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="36d4e-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36d4e-128">PARAMETERS</span></span>

### <span data-ttu-id="36d4e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d4e-129">-DefaultProfile</span></span>
<span data-ttu-id="36d4e-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36d4e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36d4e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="36d4e-131">-Force</span></span>
<span data-ttu-id="36d4e-132">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36d4e-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36d4e-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="36d4e-133">-InputFile</span></span>
<span data-ttu-id="36d4e-134">Az új szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36d4e-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="36d4e-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36d4e-135">-Namespace</span></span>
<span data-ttu-id="36d4e-136">A parancsmag által módosított engedélyezési szabályokat tartalmazó névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="36d4e-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="36d4e-137">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="36d4e-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36d4e-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36d4e-138">-ResourceGroup</span></span>
<span data-ttu-id="36d4e-139">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="36d4e-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="36d4e-140">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="36d4e-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36d4e-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="36d4e-141">-SASRule</span></span>
<span data-ttu-id="36d4e-142">Megadja a **SharedAccessAuthorizationRuleAttributes** objektumot, amely a parancsmag által módosított engedélyezési szabályok konfigurációs adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="36d4e-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d4e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d4e-143">-Confirm</span></span>
<span data-ttu-id="36d4e-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36d4e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d4e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d4e-145">-WhatIf</span></span>
<span data-ttu-id="36d4e-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36d4e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d4e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36d4e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d4e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d4e-148">CommonParameters</span></span>
<span data-ttu-id="36d4e-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d4e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d4e-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d4e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d4e-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36d4e-151">INPUTS</span></span>

### <span data-ttu-id="36d4e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="36d4e-152">System.String</span></span>

## <span data-ttu-id="36d4e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d4e-153">OUTPUTS</span></span>

### <span data-ttu-id="36d4e-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="36d4e-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="36d4e-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36d4e-155">NOTES</span></span>

## <span data-ttu-id="36d4e-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36d4e-156">RELATED LINKS</span></span>

[<span data-ttu-id="36d4e-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36d4e-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="36d4e-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36d4e-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="36d4e-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36d4e-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


