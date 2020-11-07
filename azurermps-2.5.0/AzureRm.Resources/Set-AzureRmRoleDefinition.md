---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849481"
---
# <span data-ttu-id="349c6-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="349c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="349c6-102">SYNOPSIS</span></span>
<span data-ttu-id="349c6-103">Egyéni szerepkör módosítása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="349c6-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="349c6-104">A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="349c6-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="349c6-105">Először használja a Get-AzureRmRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="349c6-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="349c6-106">Ezután módosítsa a módosítani kívánt tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="349c6-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="349c6-107">Végül mentse a szerepkör-definíciót a parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="349c6-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="349c6-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="349c6-108">SYNTAX</span></span>

### <span data-ttu-id="349c6-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="349c6-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="349c6-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="349c6-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="349c6-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="349c6-111">DESCRIPTION</span></span>
<span data-ttu-id="349c6-112">A Set-AzureRmRoleDefinition parancsmag egy meglévő egyéni szerepkört frissít az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="349c6-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="349c6-113">Adja meg a frissített szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="349c6-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="349c6-114">A frissített egyéni szerepkör szerepkör-definíciójának tartalmaznia kell a szerepkör azonosítóját és minden egyéb szükséges tulajdonságát, még ha nem is frissítik: DisplayName, leírás, műveletek és AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="349c6-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="349c6-115">A DataActions, a NotDataActions nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="349c6-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="349c6-116">A következőkben a példa frissítve: JSON for Set-AzureRmRoleDefinition {"azonosító": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "név": "frissítve role", "Description": "figyelemmel kísérheti az összes erőforrást, és indítsa el és indítsa újra a virtuális gépeket", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}</span><span class="sxs-lookup"><span data-stu-id="349c6-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="349c6-117">Példák</span><span class="sxs-lookup"><span data-stu-id="349c6-117">EXAMPLES</span></span>

### <span data-ttu-id="349c6-118">Frissítés a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="349c6-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="349c6-119">Létrehozás JSON-fájl használatával</span><span class="sxs-lookup"><span data-stu-id="349c6-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="349c6-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="349c6-120">PARAMETERS</span></span>

### <span data-ttu-id="349c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349c6-121">-DefaultProfile</span></span>
<span data-ttu-id="349c6-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="349c6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="349c6-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="349c6-123">-InputFile</span></span>
<span data-ttu-id="349c6-124">Annak a fájlnevnek a neve, amely egyetlen JSON szerepkör-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="349c6-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="349c6-125">Csak a JSON-ban frissítendő tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="349c6-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="349c6-126">Szükség van az azonosító tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="349c6-126">Id property is Required.</span></span>

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

### <span data-ttu-id="349c6-127">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="349c6-127">-Role</span></span>
<span data-ttu-id="349c6-128">Frissítendő szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="349c6-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="349c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349c6-129">CommonParameters</span></span>
<span data-ttu-id="349c6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="349c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349c6-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349c6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349c6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="349c6-132">INPUTS</span></span>

### <span data-ttu-id="349c6-133">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="349c6-134">Paraméterek: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="349c6-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="349c6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="349c6-135">OUTPUTS</span></span>

### <span data-ttu-id="349c6-136">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="349c6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="349c6-137">NOTES</span></span>
<span data-ttu-id="349c6-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="349c6-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="349c6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="349c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="349c6-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="349c6-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="349c6-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="349c6-142">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="349c6-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="349c6-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

