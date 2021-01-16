---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466395"
---
# <span data-ttu-id="cf6e4-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="cf6e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6e4-103">Módosít egy egyéni szerepkört az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="cf6e4-104">Adja meg a módosított szerepkör-definíciót JSON-fájlként vagy PSRoleDefinition formátumban.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="cf6e4-105">Először a Get-AzRoleDefinition paranccsal olvassa be a módosítani kívánt egyéni szerepkört.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="cf6e4-106">Ezután módosítsa a módosítani kívánt tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="cf6e4-107">Végül ezzel a paranccsal mentse a szerepkördefiníciót.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="cf6e4-108">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf6e4-108">SYNTAX</span></span>

### <span data-ttu-id="cf6e4-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf6e4-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf6e4-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf6e4-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf6e4-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf6e4-111">DESCRIPTION</span></span>
<span data-ttu-id="cf6e4-112">A Set-AzRoleDefinition parancsmag frissíti a meglévő egyéni szerepkört az Azure Role-Based Hozzáférés-vezérlésben.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="cf6e4-113">Adja meg a frissített szerepkördefiníciót bemenetként a parancshoz JSON-fájlként vagy PSRoleDefinition objektumként.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="cf6e4-114">A frissített egyéni szerepkör szerepkördefiníciójának tartalmaznia kell a szerepkör azonosítóját és minden más szükséges tulajdonságát, még akkor is, ha nem frissülnek: DisplayName, Leírás, Műveletek, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="cf6e4-115">A NotActions, a DataActions és a NotDataActions paraméter megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="cf6e4-116">Az alábbiakban egy json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Műveletek": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="cf6e4-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="cf6e4-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf6e4-117">EXAMPLES</span></span>

### <span data-ttu-id="cf6e4-118">1. példa: Frissítés a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="cf6e4-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="cf6e4-119">2. példa: Létrehozás JSON-fájllal</span><span class="sxs-lookup"><span data-stu-id="cf6e4-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="cf6e4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf6e4-120">PARAMETERS</span></span>

### <span data-ttu-id="cf6e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6e4-121">-DefaultProfile</span></span>
<span data-ttu-id="cf6e4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cf6e4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf6e4-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cf6e4-123">-InputFile</span></span>
<span data-ttu-id="cf6e4-124">A frissíthető json szerepkördefiníciót tartalmazó fájlnév.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="cf6e4-125">Csak azok a tulajdonságok szerepeljenek, amelyek frissítve vannak a JSON-ban.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="cf6e4-126">Id tulajdonság kötelező.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf6e4-127">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="cf6e4-127">-Role</span></span>
<span data-ttu-id="cf6e4-128">Frissítend kell a szerepkör-definíciós objektumot</span><span class="sxs-lookup"><span data-stu-id="cf6e4-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6e4-129">CommonParameters</span></span>
<span data-ttu-id="cf6e4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf6e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6e4-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf6e4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6e4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf6e4-132">INPUTS</span></span>

### <span data-ttu-id="cf6e4-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="cf6e4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf6e4-134">OUTPUTS</span></span>

### <span data-ttu-id="cf6e4-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="cf6e4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf6e4-136">NOTES</span></span>
<span data-ttu-id="cf6e4-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="cf6e4-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cf6e4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf6e4-138">RELATED LINKS</span></span>

[<span data-ttu-id="cf6e4-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="cf6e4-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="cf6e4-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="cf6e4-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="cf6e4-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cf6e4-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

