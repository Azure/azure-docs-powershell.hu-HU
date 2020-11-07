---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: f0c22f199d19e97f957bc86fbee8d649d30b622d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680005"
---
# <span data-ttu-id="245cc-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="245cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="245cc-102">SYNOPSIS</span></span>
<span data-ttu-id="245cc-103">Egyéni szerepkör módosítása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="245cc-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="245cc-104">A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="245cc-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="245cc-105">Először használja a Get-AzureRmRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="245cc-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="245cc-106">Ezután módosítsa a módosítani kívánt tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="245cc-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="245cc-107">Végül mentse a szerepkör-definíciót a parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="245cc-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="245cc-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="245cc-108">SYNTAX</span></span>

### <span data-ttu-id="245cc-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="245cc-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="245cc-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="245cc-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="245cc-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="245cc-111">DESCRIPTION</span></span>
<span data-ttu-id="245cc-112">A Set-AzureRmRoleDefinition parancsmag egy meglévő egyéni szerepkört frissít az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="245cc-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="245cc-113">Adja meg a frissített szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="245cc-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="245cc-114">A frissített egyéni szerepkör szerepkör-definíciójának tartalmaznia kell a szerepkör azonosítóját és minden egyéb szükséges tulajdonságát, még ha nem is frissítik: DisplayName, leírás, műveletek és AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="245cc-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="245cc-115">A DataActions, a NotDataActions nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="245cc-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="245cc-116">A következőkben a példa frissítve: JSON for Set-AzureRmRoleDefinition {"azonosító": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "név": "frissítve role", "Description": "figyelemmel kísérheti az összes erőforrást, és indítsa el és indítsa újra a virtuális gépeket", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}</span><span class="sxs-lookup"><span data-stu-id="245cc-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="245cc-117">Példák</span><span class="sxs-lookup"><span data-stu-id="245cc-117">EXAMPLES</span></span>

### <span data-ttu-id="245cc-118">Frissítés a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="245cc-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="245cc-119">Létrehozás JSON-fájl használatával</span><span class="sxs-lookup"><span data-stu-id="245cc-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="245cc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="245cc-120">PARAMETERS</span></span>

### <span data-ttu-id="245cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245cc-121">-DefaultProfile</span></span>
<span data-ttu-id="245cc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="245cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="245cc-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="245cc-123">-InputFile</span></span>
<span data-ttu-id="245cc-124">Annak a fájlnevnek a neve, amely egyetlen JSON szerepkör-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="245cc-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="245cc-125">Csak a JSON-ban frissítendő tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="245cc-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="245cc-126">Szükség van az azonosító tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="245cc-126">Id property is Required.</span></span>

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

### <span data-ttu-id="245cc-127">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="245cc-127">-Role</span></span>
<span data-ttu-id="245cc-128">Frissítendő szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="245cc-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="245cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245cc-129">CommonParameters</span></span>
<span data-ttu-id="245cc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="245cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245cc-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245cc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="245cc-132">INPUTS</span></span>

### <span data-ttu-id="245cc-133">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="245cc-134">Paraméterek: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="245cc-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="245cc-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="245cc-135">OUTPUTS</span></span>

### <span data-ttu-id="245cc-136">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="245cc-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="245cc-137">NOTES</span></span>
<span data-ttu-id="245cc-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="245cc-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="245cc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="245cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="245cc-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="245cc-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="245cc-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="245cc-142">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="245cc-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="245cc-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

