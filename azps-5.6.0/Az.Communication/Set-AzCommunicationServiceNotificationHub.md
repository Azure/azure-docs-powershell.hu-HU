---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: 1dbdbc6a616e9903c6a79192d089ea959835a9f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938929"
---
# <span data-ttu-id="6d7e2-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6d7e2-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="6d7e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7e2-103">Egy Azure értesítési központot erre a kommunikációs szolgáltatásra mutató hivatkozásokkal hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="6d7e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d7e2-104">SYNTAX</span></span>

### <span data-ttu-id="6d7e2-105">LinkExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d7e2-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6d7e2-106">Hivatkozás</span><span class="sxs-lookup"><span data-stu-id="6d7e2-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d7e2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d7e2-107">DESCRIPTION</span></span>
<span data-ttu-id="6d7e2-108">Egy Azure értesítési központot erre a kommunikációs szolgáltatásra mutató hivatkozásokkal hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="6d7e2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d7e2-109">EXAMPLES</span></span>

### <span data-ttu-id="6d7e2-110">1. példa: Az értesítési központ részleteinek interaktív megküldése</span><span class="sxs-lookup"><span data-stu-id="6d7e2-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="6d7e2-111">A csatolt értesítési központ lehetővé teszi az ACS-erőforrásoknak, hogy bizonyos eseményekről értesítéseket küldjenek.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="6d7e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d7e2-112">PARAMETERS</span></span>

### <span data-ttu-id="6d7e2-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="6d7e2-113">-CommunicationServiceName</span></span>
<span data-ttu-id="6d7e2-114">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6d7e2-115">-ConnectionString</span></span>
<span data-ttu-id="6d7e2-116">Az értesítési központ kapcsolati karakterlánca</span><span class="sxs-lookup"><span data-stu-id="6d7e2-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7e2-117">-DefaultProfile</span></span>
<span data-ttu-id="6d7e2-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="6d7e2-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="6d7e2-120">Annak az Azure Értesítési központnak a leírása, amely csatolva van a létrehozni szükséges kommunikációs szolgáltatáshoz, a NOTES (JEGYZETEK) szakaszban találja a LINKNOTIFICATIONHUBPARAMETER tulajdonságokat, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6d7e2-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="6d7e2-122">Az értesítési központ erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6d7e2-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d7e2-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d7e2-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d7e2-126">-SubscriptionId</span></span>
<span data-ttu-id="6d7e2-127">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d7e2-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7e2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d7e2-129">-Confirm</span></span>
<span data-ttu-id="6d7e2-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d7e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7e2-131">-WhatIf</span></span>
<span data-ttu-id="6d7e2-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7e2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d7e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7e2-134">CommonParameters</span></span>
<span data-ttu-id="6d7e2-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7e2-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d7e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7e2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d7e2-137">INPUTS</span></span>

### <span data-ttu-id="6d7e2-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="6d7e2-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="6d7e2-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d7e2-139">OUTPUTS</span></span>

### <span data-ttu-id="6d7e2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6d7e2-140">System.String</span></span>

## <span data-ttu-id="6d7e2-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d7e2-141">NOTES</span></span>

<span data-ttu-id="6d7e2-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6d7e2-142">ALIASES</span></span>

<span data-ttu-id="6d7e2-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6d7e2-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d7e2-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d7e2-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d7e2-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d7e2-146">LINKNOTIFICATIONHUBPARAMETER: A kommunikációs szolgáltatáshoz csatoló Azure értesítési központ <ILinkNotificationHubParameters> leírása</span><span class="sxs-lookup"><span data-stu-id="6d7e2-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="6d7e2-147">`ConnectionString <String>`: Az értesítési központ kapcsolati karakterlánca</span><span class="sxs-lookup"><span data-stu-id="6d7e2-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="6d7e2-148">`ResourceId <String>`: Az értesítési központ erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6d7e2-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="6d7e2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d7e2-149">RELATED LINKS</span></span>

