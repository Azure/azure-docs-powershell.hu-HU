---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466436"
---
# <span data-ttu-id="b3889-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b3889-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="b3889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3889-102">SYNOPSIS</span></span>
<span data-ttu-id="b3889-103">Egyéni szerepkört hoz létre az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="b3889-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b3889-104">Adjon meg JSON szerepkördefiníciós fájlt vagy PSRoleDefinition objektumot bemenetként.</span><span class="sxs-lookup"><span data-stu-id="b3889-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="b3889-105">Először a Get-AzRoleDefinition paranccsal hozzon létre egy alaptervi szerepkör-definíciós objektumot.</span><span class="sxs-lookup"><span data-stu-id="b3889-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="b3889-106">Ezután szükség szerint módosítsa a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b3889-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="b3889-107">Végül ezzel a paranccsal szerepkördefiníció használatával hozhat létre egyéni szerepkört.</span><span class="sxs-lookup"><span data-stu-id="b3889-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="b3889-108">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3889-108">SYNTAX</span></span>

### <span data-ttu-id="b3889-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3889-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3889-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3889-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3889-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3889-111">DESCRIPTION</span></span>
<span data-ttu-id="b3889-112">A New-AzRoleDefinition parancsmag létrehoz egy egyéni szerepkört az Azure Role-Based Hozzáférés-vezérlésben.</span><span class="sxs-lookup"><span data-stu-id="b3889-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b3889-113">Adjon meg szerepkördefiníciót a parancs bemeneteként JSON-fájlként vagy PSRoleDefinition objektumként.</span><span class="sxs-lookup"><span data-stu-id="b3889-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="b3889-114">A bemeneti szerepkör definíciójának az alábbi tulajdonságokat kell tartalmaznia:</span><span class="sxs-lookup"><span data-stu-id="b3889-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="b3889-115">DisplayName: az egyéni szerepkör neve</span><span class="sxs-lookup"><span data-stu-id="b3889-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="b3889-116">Leírás: a szerepkör rövid leírása, amely összegzi a szerepkör által nyújtott hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="b3889-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="b3889-117">Műveletek: az a műveletkészlet, amelyhez az egyéni szerepkör hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="b3889-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="b3889-118">A Get-AzProviderOperation azure-erőforrás-szolgáltatók azure RBAC-n keresztül is biztonságos műveleteket használhatja.</span><span class="sxs-lookup"><span data-stu-id="b3889-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="b3889-119">Az alábbiakban néhány érvényes műveleti karakterláncot is be kell íme:</span><span class="sxs-lookup"><span data-stu-id="b3889-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="b3889-120">A "\*/read" hozzáféréssel rendelkezik az összes Azure-erőforrásszolgáltató olvasási műveleteihez.</span><span class="sxs-lookup"><span data-stu-id="b3889-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="b3889-121">A "Microsoft.Network/\*/read" olvasási műveletekhez biztosít hozzáférést az Azure Microsoft.Network erőforrásszolgáltatójának összes erőforrástípusához.</span><span class="sxs-lookup"><span data-stu-id="b3889-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="b3889-122">A "Microsoft.Compute/virtualMachines/\*" hozzáférést biztosít a virtuális gépek és a gyermekerőforrás-típusok minden művelethez.</span><span class="sxs-lookup"><span data-stu-id="b3889-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="b3889-123">AssignableScopes: az a hatókörcsoport (Azure-előfizetések vagy erőforráscsoportok), amelyekben az egyéni szerepkör elérhető lesz a hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="b3889-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="b3889-124">A AssignableScopes használatával az egyéni szerepkört csak az előfizetések vagy erőforráscsoportok számára teszi elérhetővé, a többi előfizetés vagy erőforráscsoport felhasználói élményét nem.</span><span class="sxs-lookup"><span data-stu-id="b3889-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="b3889-125">Íme néhány érvényes hozzárendelhető hatókör:</span><span class="sxs-lookup"><span data-stu-id="b3889-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="b3889-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": két előfizetésben elérhetővé teszi a szerepkört a hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="b3889-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="b3889-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": elérhetővé teszi a szerepkört egyetlen előfizetésben való hozzárendeléshez.</span><span class="sxs-lookup"><span data-stu-id="b3889-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="b3889-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": csak a Hálózati erőforráscsoportban teszi elérhetővé a hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="b3889-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="b3889-129">A bemeneti szerepkör definíciója az alábbi tulajdonságokat tartalmazhatja:</span><span class="sxs-lookup"><span data-stu-id="b3889-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="b3889-130">NotActions: azok a műveletek, amelyekből ki kell zárni az egyéni szerepkör tényleges műveleteinek meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="b3889-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="b3889-131">Ha van egy olyan művelet, amelyhez nem szeretne hozzáférést adni egy egyéni szerepkörben, a NotActions segítségével egyszerűen kizárhatja azt, nem kell megadnia az adott műveleten kívül az összes műveletet a Műveletekben.</span><span class="sxs-lookup"><span data-stu-id="b3889-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="b3889-132">DataActions: az az adatművelet-készlet, amelyhez az egyéni szerepkör hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="b3889-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="b3889-133">NotDataActions: azok a műveletek, amelyekből ki kell zárni a DataActions műveletből az egyéni szerepkör hatékony adatműveletének meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="b3889-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="b3889-134">Ha van egy olyan adatművelet, amelyhez nem szeretne hozzáférést adni egy egyéni szerepkörben, a NotDataActions segítségével kizárhatja a műveletet, és nem kell az adott műveleten kívül más műveleteket megadnia a Műveletekben.</span><span class="sxs-lookup"><span data-stu-id="b3889-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="b3889-135">MEGJEGYZÉS: Ha egy felhasználóhoz olyan szerepkör van hozzárendelve, amely a NotActions műveletben meghatároz egy műveletet, és egy másik szerepkör is hozzáférést biztosít ugyanannak a műveletnek – a felhasználó képes lesz végrehajtani ezt a műveletet.</span><span class="sxs-lookup"><span data-stu-id="b3889-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="b3889-136">A NotActions nem elutasítási szabály – egyszerűen kényelmes módja az engedélyezett műveletek halmazának létrehozásához, ha bizonyos műveleteket ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="b3889-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="b3889-137">Az alábbiakban egy json szerepkördefiníciót tartalmazó minta található, amely bevitelként meg lehet adni a következőt: { "Név": "Frissített szerepkör", "Leírás": "Figyelheti az összes erőforrást, és elindíthatja és újraindíthatja a virtuális gépeket", "Műveletek": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/container blobs/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="b3889-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="b3889-138">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3889-138">EXAMPLES</span></span>

### <span data-ttu-id="b3889-139">1. példa: Létrehozás a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="b3889-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="b3889-140">2. példa: Létrehozás JSON-fájllal</span><span class="sxs-lookup"><span data-stu-id="b3889-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="b3889-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3889-141">PARAMETERS</span></span>

### <span data-ttu-id="b3889-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3889-142">-DefaultProfile</span></span>
<span data-ttu-id="b3889-143">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b3889-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3889-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b3889-144">-InputFile</span></span>
<span data-ttu-id="b3889-145">Egy json-szerepkördefiníciót tartalmazó fájlnév.</span><span class="sxs-lookup"><span data-stu-id="b3889-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3889-146">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="b3889-146">-Role</span></span>
<span data-ttu-id="b3889-147">Szerepkör-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="b3889-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3889-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3889-148">CommonParameters</span></span>
<span data-ttu-id="b3889-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3889-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3889-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3889-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3889-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3889-151">INPUTS</span></span>

### <span data-ttu-id="b3889-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3889-152">None</span></span>

## <span data-ttu-id="b3889-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3889-153">OUTPUTS</span></span>

### <span data-ttu-id="b3889-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b3889-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b3889-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3889-155">NOTES</span></span>
<span data-ttu-id="b3889-156">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="b3889-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b3889-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3889-157">RELATED LINKS</span></span>

[<span data-ttu-id="b3889-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b3889-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="b3889-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b3889-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="b3889-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b3889-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="b3889-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b3889-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

