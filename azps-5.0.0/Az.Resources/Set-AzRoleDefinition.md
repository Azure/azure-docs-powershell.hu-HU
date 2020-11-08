---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195517"
---
# <span data-ttu-id="24c51-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="24c51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24c51-102">SYNOPSIS</span></span>
<span data-ttu-id="24c51-103">Egyéni szerepkör módosítása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="24c51-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="24c51-104">A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="24c51-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="24c51-105">Először használja a Get-AzRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="24c51-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="24c51-106">Ezután módosítsa a módosítani kívánt tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="24c51-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="24c51-107">Végül mentse a szerepkör-definíciót a parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="24c51-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="24c51-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24c51-108">SYNTAX</span></span>

### <span data-ttu-id="24c51-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c51-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c51-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c51-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c51-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="24c51-111">DESCRIPTION</span></span>
<span data-ttu-id="24c51-112">A Set-AzRoleDefinition parancsmag egy meglévő egyéni szerepkört frissít az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="24c51-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="24c51-113">Adja meg a frissített szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="24c51-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="24c51-114">A frissített egyéni szerepkör szerepkör-definíciójának tartalmaznia kell a szerepkör azonosítóját és minden egyéb szükséges tulajdonságát, még ha nem is frissítik: DisplayName, leírás, műveletek és AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="24c51-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="24c51-115">A DataActions, a NotDataActions nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24c51-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="24c51-116">A következőkben a példa frissítve: JSON for Set-AzRoleDefinition {"azonosító": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "név": "frissítve role", "Description": "figyelemmel kísérheti az összes erőforrást, és indítsa el és indítsa újra a virtuális gépeket", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}</span><span class="sxs-lookup"><span data-stu-id="24c51-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="24c51-117">Példák</span><span class="sxs-lookup"><span data-stu-id="24c51-117">EXAMPLES</span></span>

### <span data-ttu-id="24c51-118">1. példa: frissítés a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="24c51-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="24c51-119">2. példa: létrehozás JSON-fájl használatával</span><span class="sxs-lookup"><span data-stu-id="24c51-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="24c51-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24c51-120">PARAMETERS</span></span>

### <span data-ttu-id="24c51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c51-121">-DefaultProfile</span></span>
<span data-ttu-id="24c51-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24c51-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c51-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="24c51-123">-InputFile</span></span>
<span data-ttu-id="24c51-124">Annak a fájlnevnek a neve, amely egyetlen JSON szerepkör-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="24c51-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="24c51-125">Csak a JSON-ban frissítendő tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="24c51-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="24c51-126">Szükség van az azonosító tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="24c51-126">Id property is Required.</span></span>

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

### <span data-ttu-id="24c51-127">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="24c51-127">-Role</span></span>
<span data-ttu-id="24c51-128">Frissítendő szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="24c51-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="24c51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c51-129">CommonParameters</span></span>
<span data-ttu-id="24c51-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24c51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c51-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24c51-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c51-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24c51-132">INPUTS</span></span>

### <span data-ttu-id="24c51-133">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="24c51-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24c51-134">OUTPUTS</span></span>

### <span data-ttu-id="24c51-135">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="24c51-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24c51-136">NOTES</span></span>
<span data-ttu-id="24c51-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="24c51-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="24c51-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24c51-138">RELATED LINKS</span></span>

[<span data-ttu-id="24c51-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="24c51-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="24c51-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="24c51-141">Új – AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="24c51-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24c51-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)
