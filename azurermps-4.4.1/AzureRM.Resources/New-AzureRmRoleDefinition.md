---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500736"
---
# <span data-ttu-id="8048f-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8048f-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="8048f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8048f-102">SYNOPSIS</span></span>
<span data-ttu-id="8048f-103">Egyéni szerepkör létrehozása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="8048f-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="8048f-104">JSON-Szerepdefiníció vagy PSRoleDefinition-objektum megadása bemenetként.</span><span class="sxs-lookup"><span data-stu-id="8048f-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="8048f-105">Első lépésként a Get-AzureRmRoleDefinition parancs segítségével hozzon létre egy eredeti szerepkör-definíciós objektumot.</span><span class="sxs-lookup"><span data-stu-id="8048f-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="8048f-106">Ezután szükség szerint módosítsa a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="8048f-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="8048f-107">Végül ezt a parancsot használva egyéni szerepkört hozhat létre a szerepkör-definícióval.</span><span class="sxs-lookup"><span data-stu-id="8048f-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8048f-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8048f-108">SYNTAX</span></span>

### <span data-ttu-id="8048f-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8048f-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8048f-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8048f-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8048f-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="8048f-111">DESCRIPTION</span></span>
<span data-ttu-id="8048f-112">A New-AzureRmRoleDefinition parancsmag egyéni szerepkört hoz létre az Azure Role-Based hozzáférés-vezérlésben.</span><span class="sxs-lookup"><span data-stu-id="8048f-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="8048f-113">Adjon meg egy szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="8048f-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="8048f-114">A beviteli szerepkör definíciójának a következő tulajdonságokat kell tartalmaznia:</span><span class="sxs-lookup"><span data-stu-id="8048f-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="8048f-115">DisplayName: az egyéni szerepkör neve</span><span class="sxs-lookup"><span data-stu-id="8048f-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="8048f-116">Leírás: annak a szerepkörnek a rövid leírása, amely összefoglalja a szerepkör által nyújtott hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8048f-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="8048f-117">Műveletek: azok a műveletek, amelyekre az egyéni szerepkör hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="8048f-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="8048f-118">Az Azure RBAC-hoz védett Azure Resource Providers műveletek megszerzéséhez használja a Get-AzureRmProviderOperations.</span><span class="sxs-lookup"><span data-stu-id="8048f-118">Use Get-AzureRmProviderOperations to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="8048f-119">Az alábbiakban néhány érvényes műveleti karakterláncot ismertetünk:</span><span class="sxs-lookup"><span data-stu-id="8048f-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="8048f-120">a "\*/READ" minden Azure Resource Provider olvasási műveletéhez hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="8048f-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="8048f-121">A "Microsoft. hálózat/\*/Read" a Microsoft. Network Resource szolgáltatója minden erőforrás-típusához hozzáférést biztosít az olvasási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="8048f-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="8048f-122">A "Microsoft. számítási/virtualMachines/\*" hozzáférést biztosít a virtuális gépek minden műveletéhez és a gyermek erőforrás-típusához.</span><span class="sxs-lookup"><span data-stu-id="8048f-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="8048f-123">AssignableScopes: azon hatókörök (Azure-előfizetések vagy erőforráscsoportok) halmaza, amelyekben az egyéni szerepkör elérhetővé válik a hozzárendelésekhez.</span><span class="sxs-lookup"><span data-stu-id="8048f-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="8048f-124">A AssignableScopes használatával az egyéni szerepkör csak azokat az előfizetéseket és erőforráscsoportokat teszi elérhetővé, amelyeknek szüksége van rá, és nem rendezheti a felhasználói felületet az előfizetések és az erőforráscsoportok többi részében.</span><span class="sxs-lookup"><span data-stu-id="8048f-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="8048f-125">A következő érvényes hozzárendelés-hatókörök használhatók:</span><span class="sxs-lookup"><span data-stu-id="8048f-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="8048f-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": a szerepkör elérhetővé tétele két előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8048f-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="8048f-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": egyetlen előfizetésben elérhetővé teszi a feladatot.</span><span class="sxs-lookup"><span data-stu-id="8048f-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="8048f-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": a szerepkör elérhetővé tétele csak a hálózati erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="8048f-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="8048f-129">A beviteli szerepkör definíciója a következő tulajdonságokat tartalmazhatja:</span><span class="sxs-lookup"><span data-stu-id="8048f-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="8048f-130">Nem megfelelő: az egyéni szerepkörhöz tartozó hatékony műveletek meghatározására szolgáló műveletek körét.</span><span class="sxs-lookup"><span data-stu-id="8048f-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="8048f-131">Ha egy olyan műveletről van szó, amely nem kíván hozzáférést biztosítani egy egyéni szerepkörben, akkor célszerű, ha nem kívánja kizárni a hozzáférést, hanem az összes műveletet nem adja meg, mint az adott műveletet a műveletek során.</span><span class="sxs-lookup"><span data-stu-id="8048f-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="8048f-132">Megjegyzés: Ha egy felhasználóhoz olyan szerepkör van társítva, amely egy olyan szerepkört ad meg, amely egy olyan művelethez van társítva, amelyhez egy másik szerepkör van társítva, akkor a felhasználó a művelet végrehajtását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="8048f-132">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="8048f-133">A nem megtagadási szabály: egyszerűen célszerű az engedélyezett műveletek halmazát kizárni, ha bizonyos műveleteket ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="8048f-133">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="8048f-134">A következőkben egy példa JSON szerepkör-definíció ("név"), "contoso on-Call", "Leírás": "a számítások, a hálózat és a tárterület figyelése, valamint a virtuális gépek újraindítása", "műveletek": \[ "Microsoft. számítási/ */READ", "Microsoft. számítási/virtualMachines/Start/Action", "Microsoft. számítási/virtualMachines/restart/Action", "Microsoft. számítási/VirtualMachines/downloadRemoteDesktopConnectionFile/Action", "Microsoft. hálózat/* /Read", "Microsoft. Storage/ */READ", "Microsoft. Authorization/* /Read", "Microsoft. Resources/Subscriptions/resourceGroups/Read", "Microsoft. Resources/Subscriptions/resourceGroups", "alertRules", "AssignableScopes" *", "Microsoft.Support/* \] \[ }, "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" \] }</span><span class="sxs-lookup"><span data-stu-id="8048f-134">Following is a sample json role definition that can be provided as input { "Name": "Contoso On-call", "Description": "Can monitor compute, network and storage, and restart virtual machines", "Actions": \[ "Microsoft.Compute/ */read", "Microsoft.Compute/virtualMachines/start/action", "Microsoft.Compute/virtualMachines/restart/action", "Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action", "Microsoft.Network/* /read", "Microsoft.Storage/ */read", "Microsoft.Authorization/* /read", "Microsoft.Resources/subscriptions/resourceGroups/read", "Microsoft.Resources/subscriptions/resourceGroups/resources/read", "Microsoft.Insights/alertRules/ *", "Microsoft.Support/* " \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx","/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"\] }</span></span>

## <span data-ttu-id="8048f-135">Példák</span><span class="sxs-lookup"><span data-stu-id="8048f-135">EXAMPLES</span></span>

### <span data-ttu-id="8048f-136">--------------------------Létrehozás a PSRoleDefinitionObject használatával--------------------------</span><span class="sxs-lookup"><span data-stu-id="8048f-136">--------------------------  Create using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="8048f-137">A--------------------------JSON-fájl használatával hozza létre--------------------------</span><span class="sxs-lookup"><span data-stu-id="8048f-137">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="8048f-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8048f-138">PARAMETERS</span></span>

### <span data-ttu-id="8048f-139">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8048f-139">-InputFile</span></span>
<span data-ttu-id="8048f-140">Egyetlen JSON-szerepkört tartalmazó fájlnév</span><span class="sxs-lookup"><span data-stu-id="8048f-140">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="8048f-141">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="8048f-141">-Role</span></span>
<span data-ttu-id="8048f-142">Szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="8048f-142">Role definition object.</span></span>

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

### <span data-ttu-id="8048f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8048f-143">-DefaultProfile</span></span>
<span data-ttu-id="8048f-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8048f-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8048f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8048f-145">CommonParameters</span></span>
<span data-ttu-id="8048f-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8048f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8048f-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8048f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8048f-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8048f-148">INPUTS</span></span>

## <span data-ttu-id="8048f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8048f-149">OUTPUTS</span></span>

### <span data-ttu-id="8048f-150">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8048f-150">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="8048f-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8048f-151">NOTES</span></span>
<span data-ttu-id="8048f-152">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="8048f-152">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8048f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8048f-153">RELATED LINKS</span></span>

[<span data-ttu-id="8048f-154">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="8048f-154">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="8048f-155">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8048f-155">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="8048f-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8048f-156">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="8048f-157">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8048f-157">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

