---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350622"
---
# <span data-ttu-id="696fa-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="696fa-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="696fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696fa-102">SYNOPSIS</span></span>
<span data-ttu-id="696fa-103">Eltávolítja az értesítési központ névterét.</span><span class="sxs-lookup"><span data-stu-id="696fa-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="696fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="696fa-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="696fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="696fa-105">DESCRIPTION</span></span>
<span data-ttu-id="696fa-106">A **Remove-AzNotificationHubsNamespace** parancsmag eltávolítja az értesítési központ névterét a telepítésből.</span><span class="sxs-lookup"><span data-stu-id="696fa-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="696fa-107">A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.</span><span class="sxs-lookup"><span data-stu-id="696fa-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="696fa-108">A **Remove-AzNotificationHubsNamespace** parancsmag eltávolítja az értesítési központ névterét a telepítésből.</span><span class="sxs-lookup"><span data-stu-id="696fa-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="696fa-109">A parancsmag futtatásakor a megadott névtér az adott névtérhez társított értesítési központokkal együtt törlődik.</span><span class="sxs-lookup"><span data-stu-id="696fa-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="696fa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="696fa-110">EXAMPLES</span></span>

### <span data-ttu-id="696fa-111">1. példa: Értesítési központ névterének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="696fa-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="696fa-112">Ez a parancs eltávolítja a ContosoNamespace nevű névteret.</span><span class="sxs-lookup"><span data-stu-id="696fa-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="696fa-113">Meg kell adnia azt az erőforráscsoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="696fa-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="696fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696fa-114">PARAMETERS</span></span>

### <span data-ttu-id="696fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696fa-115">-DefaultProfile</span></span>
<span data-ttu-id="696fa-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="696fa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="696fa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="696fa-117">-Force</span></span>
<span data-ttu-id="696fa-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="696fa-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="696fa-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="696fa-119">-Namespace</span></span>
<span data-ttu-id="696fa-120">A parancsmag által eltávolított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="696fa-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="696fa-121">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="696fa-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="696fa-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="696fa-122">-ResourceGroup</span></span>
<span data-ttu-id="696fa-123">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="696fa-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="696fa-124">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="696fa-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="696fa-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="696fa-125">-Confirm</span></span>
<span data-ttu-id="696fa-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="696fa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696fa-127">-WhatIf</span></span>
<span data-ttu-id="696fa-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="696fa-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="696fa-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="696fa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696fa-130">CommonParameters</span></span>
<span data-ttu-id="696fa-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696fa-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696fa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696fa-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="696fa-133">INPUTS</span></span>

### <span data-ttu-id="696fa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="696fa-134">System.String</span></span>

## <span data-ttu-id="696fa-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="696fa-135">OUTPUTS</span></span>

### <span data-ttu-id="696fa-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="696fa-136">System.Void</span></span>

## <span data-ttu-id="696fa-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="696fa-137">NOTES</span></span>

## <span data-ttu-id="696fa-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="696fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="696fa-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="696fa-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="696fa-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="696fa-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="696fa-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="696fa-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


