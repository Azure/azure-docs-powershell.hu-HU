---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496927"
---
# <span data-ttu-id="84f43-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="84f43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84f43-102">SYNOPSIS</span></span>
<span data-ttu-id="84f43-103">Egyéni szerepkör módosítása az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="84f43-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="84f43-104">A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="84f43-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="84f43-105">Először használja a Get-AzureRmRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="84f43-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="84f43-106">Ezután módosítsa a módosítani kívánt tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="84f43-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="84f43-107">Végül mentse a szerepkör-definíciót a parancs segítségével.</span><span class="sxs-lookup"><span data-stu-id="84f43-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84f43-108">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84f43-108">SYNTAX</span></span>

### <span data-ttu-id="84f43-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f43-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84f43-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f43-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84f43-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="84f43-111">DESCRIPTION</span></span>
<span data-ttu-id="84f43-112">A Set-AzureRmRoleDefinition parancsmag egy meglévő egyéni szerepkört frissít az Azure Role-Based Access-vezérlőben.</span><span class="sxs-lookup"><span data-stu-id="84f43-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="84f43-113">Adja meg a frissített szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.</span><span class="sxs-lookup"><span data-stu-id="84f43-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="84f43-114">A frissített egyéni szerepkör szerepkör-definíciójának tartalmaznia kell a szerepkör azonosítóját és minden egyéb szükséges tulajdonságát, még ha nem is frissítik: DisplayName, leírás, műveletek és AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="84f43-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="84f43-115">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="84f43-115">NotActions is optional.</span></span>

<span data-ttu-id="84f43-116">Az alábbiakban egy példa frissítve Set-AzureRmRoleDefinition JSON-hoz</span><span class="sxs-lookup"><span data-stu-id="84f43-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="84f43-117">{"Azonosító": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "név": "frissítve role", "Description": "az összes erőforrás figyelése, és a virtuális gépek indítása és újraindítása", "műveletek": \[ "\*/READ", "Microsoft. ClassicCompute/virtualmachines/restart/restart/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] "AssignableScopes": \[ "/Subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="84f43-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="84f43-118">Példák</span><span class="sxs-lookup"><span data-stu-id="84f43-118">EXAMPLES</span></span>

### <span data-ttu-id="84f43-119">--------------------------Frissítés a PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="84f43-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="84f43-120">A--------------------------JSON-fájl használatával hozza létre--------------------------</span><span class="sxs-lookup"><span data-stu-id="84f43-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="84f43-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84f43-121">PARAMETERS</span></span>

### <span data-ttu-id="84f43-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="84f43-122">-InputFile</span></span>
<span data-ttu-id="84f43-123">Annak a fájlnevnek a neve, amely egyetlen JSON szerepkör-definíciót tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="84f43-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="84f43-124">Csak a JSON-ban frissítendő tulajdonságokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="84f43-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="84f43-125">Szükség van az azonosító tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="84f43-125">Id property is Required.</span></span>

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

### <span data-ttu-id="84f43-126">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="84f43-126">-Role</span></span>
<span data-ttu-id="84f43-127">Frissítendő szerepkör-definíciós objektum</span><span class="sxs-lookup"><span data-stu-id="84f43-127">Role definition object to be updated</span></span>

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

### <span data-ttu-id="84f43-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f43-128">-DefaultProfile</span></span>
<span data-ttu-id="84f43-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84f43-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84f43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f43-130">CommonParameters</span></span>
<span data-ttu-id="84f43-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84f43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f43-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f43-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f43-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f43-133">INPUTS</span></span>

### <span data-ttu-id="84f43-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-134">PSRoleDefinition</span></span>
<span data-ttu-id="84f43-135">A "role" paraméter értéke az "PSRoleDefinition" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="84f43-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="84f43-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84f43-136">OUTPUTS</span></span>

### <span data-ttu-id="84f43-137">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="84f43-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84f43-138">NOTES</span></span>
<span data-ttu-id="84f43-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="84f43-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="84f43-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84f43-140">RELATED LINKS</span></span>

[<span data-ttu-id="84f43-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="84f43-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="84f43-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="84f43-143">Új – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="84f43-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="84f43-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

