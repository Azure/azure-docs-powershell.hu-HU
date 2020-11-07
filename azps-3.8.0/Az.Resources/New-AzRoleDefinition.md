---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 02e40cb22661d7898b9048f8e04cafdd33852994
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845878"
---
# <span data-ttu-id="7c7c4-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7c4-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="7c7c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7c4-103">Egyéni szerepkör létrehozása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="7c7c4-104">JSON-Szerepdefiníció vagy PSRoleDefinition-objektum megadása bemenetként.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="7c7c4-105">Első lépésként a Get-AzRoleDefinition parancs segítségével hozzon létre egy eredeti szerepkör-definíciós objektumot.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="7c7c4-106">Ezután szükség szerint módosítsa a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="7c7c4-107">Végül ezt a parancsot használva egyéni szerepkört hozhat létre a szerepkör-definícióval.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="7c7c4-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c7c4-108">SYNTAX</span></span>

### <span data-ttu-id="7c7c4-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c7c4-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7c4-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c7c4-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c7c4-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c7c4-111">DESCRIPTION</span></span>
<span data-ttu-id="7c7c4-112">A New-AzRoleDefinition parancsmag egyéni szerepkört hoz létre az Azure Role-Based hozzáférés-vezérlésben.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="7c7c4-113">Adjon meg egy szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="7c7c4-114">A beviteli szerepkör definíciójának a következő tulajdonságokat kell tartalmaznia:</span><span class="sxs-lookup"><span data-stu-id="7c7c4-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="7c7c4-115">DisplayName: az egyéni szerepkör neve</span><span class="sxs-lookup"><span data-stu-id="7c7c4-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="7c7c4-116">Leírás: annak a szerepkörnek a rövid leírása, amely összefoglalja a szerepkör által nyújtott hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="7c7c4-117">Műveletek: azok a műveletek, amelyekre az egyéni szerepkör hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="7c7c4-118">Az Azure RBAC-hoz védett Azure Resource Providers műveletek megszerzéséhez használja a Get-AzProviderOperation.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="7c7c4-119">Az alábbiakban néhány érvényes műveleti karakterláncot ismertetünk:</span><span class="sxs-lookup"><span data-stu-id="7c7c4-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="7c7c4-120">a "\*/READ" minden Azure Resource Provider olvasási műveletéhez hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="7c7c4-121">A "Microsoft. hálózat/\*/Read" a Microsoft. Network Resource szolgáltatója minden erőforrás-típusához hozzáférést biztosít az olvasási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="7c7c4-122">A "Microsoft. számítási/virtualMachines/\*" hozzáférést biztosít a virtuális gépek minden műveletéhez és a gyermek erőforrás-típusához.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="7c7c4-123">AssignableScopes: azon hatókörök (Azure-előfizetések vagy erőforráscsoportok) halmaza, amelyekben az egyéni szerepkör elérhetővé válik a hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="7c7c4-124">A AssignableScopes használatával az egyéni szerepkör csak azokat az előfizetéseket és erőforráscsoportokat teszi elérhetővé, amelyeknek szüksége van rá, és nem rendezheti a felhasználói felületet az előfizetések és az erőforráscsoportok többi részében.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="7c7c4-125">A következő érvényes hozzárendelés-hatókörök használhatók:</span><span class="sxs-lookup"><span data-stu-id="7c7c4-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="7c7c4-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": a szerepkör elérhetővé tétele két előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="7c7c4-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": egyetlen előfizetésben elérhetővé teszi a feladatot.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="7c7c4-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": a szerepkör elérhetővé tétele csak a hálózati erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="7c7c4-129">A beviteli szerepkör definíciója a következő tulajdonságokat tartalmazhatja:</span><span class="sxs-lookup"><span data-stu-id="7c7c4-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="7c7c4-130">Nem megfelelő: az egyéni szerepkörhöz tartozó hatékony műveletek meghatározására szolgáló műveletek körét.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="7c7c4-131">Ha egy olyan műveletről van szó, amely nem kíván hozzáférést biztosítani egy egyéni szerepkörben, akkor célszerű, ha nem kívánja kizárni a hozzáférést, hanem az összes műveletet nem adja meg, mint az adott műveletet a műveletek során.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="7c7c4-132">DataActions: azoknak az adatműveleteknek a halmaza, amelyekhez az egyéni szerepkör hozzáférést ad.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="7c7c4-133">NotDataActions: azoknak a műveleteknek a halmazát, amelyeket ki kell zárni a DataActions, és meg kell határozni az egyéni szerepkörhöz tartozó hatékony adatműveleteket.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="7c7c4-134">Ha egy olyan adatműveletről van szó, amely nem kíván hozzáférést adni egy egyéni szerepkörhöz, célszerű a NotDataActions használni, és nem az összes műveletet megadni, mint az adott műveleten kívüli műveletek.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="7c7c4-135">Megjegyzés: Ha egy felhasználóhoz olyan szerepkör van társítva, amely egy olyan szerepkört ad meg, amely egy olyan művelethez van társítva, amelyhez egy másik szerepkör van társítva, akkor a felhasználó a művelet végrehajtását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="7c7c4-136">A nem megtagadási szabály: egyszerűen célszerű az engedélyezett műveletek halmazát kizárni, ha bizonyos műveleteket ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="7c7c4-137">A következőkben egy példa JSON szerepkör-definíció ("név") érhető el: "updated role", "Description": "az összes erőforrás figyelése, valamint a virtuális gépek indítása és újraindítása", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}</span><span class="sxs-lookup"><span data-stu-id="7c7c4-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="7c7c4-138">Példák</span><span class="sxs-lookup"><span data-stu-id="7c7c4-138">EXAMPLES</span></span>

### <span data-ttu-id="7c7c4-139">Létrehozás a PSRoleDefinitionObject használatával</span><span class="sxs-lookup"><span data-stu-id="7c7c4-139">Create using PSRoleDefinitionObject</span></span>
```
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

### <span data-ttu-id="7c7c4-140">Létrehozás JSON-fájl használatával</span><span class="sxs-lookup"><span data-stu-id="7c7c4-140">Create using JSON file</span></span>
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="7c7c4-141">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c7c4-141">PARAMETERS</span></span>

### <span data-ttu-id="7c7c4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7c4-142">-DefaultProfile</span></span>
<span data-ttu-id="7c7c4-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c7c4-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c7c4-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7c7c4-144">-InputFile</span></span>
<span data-ttu-id="7c7c4-145">Egyetlen JSON-szerepkört tartalmazó fájlnév</span><span class="sxs-lookup"><span data-stu-id="7c7c4-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="7c7c4-146">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="7c7c4-146">-Role</span></span>
<span data-ttu-id="7c7c4-147">Szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="7c7c4-147">Role definition object.</span></span>

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

### <span data-ttu-id="7c7c4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7c4-148">CommonParameters</span></span>
<span data-ttu-id="7c7c4-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c7c4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7c4-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c7c4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7c4-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c7c4-151">INPUTS</span></span>

### <span data-ttu-id="7c7c4-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c7c4-152">None</span></span>

## <span data-ttu-id="7c7c4-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c7c4-153">OUTPUTS</span></span>

### <span data-ttu-id="7c7c4-154">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7c4-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7c7c4-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c7c4-155">NOTES</span></span>
<span data-ttu-id="7c7c4-156">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="7c7c4-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7c7c4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c7c4-157">RELATED LINKS</span></span>

[<span data-ttu-id="7c7c4-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="7c7c4-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="7c7c4-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7c4-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="7c7c4-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7c4-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="7c7c4-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7c4-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

