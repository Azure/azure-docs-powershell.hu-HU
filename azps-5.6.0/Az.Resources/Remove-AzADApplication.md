---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: d4415b2f97cb92c8694c0ca56a3b47d751a065f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936098"
---
# <span data-ttu-id="b2d75-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2d75-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="b2d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d75-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d75-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b2d75-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="b2d75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2d75-104">SYNTAX</span></span>

### <span data-ttu-id="b2d75-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2d75-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2d75-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2d75-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2d75-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2d75-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2d75-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2d75-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d75-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2d75-109">DESCRIPTION</span></span>
<span data-ttu-id="b2d75-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b2d75-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="b2d75-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2d75-111">EXAMPLES</span></span>

### <span data-ttu-id="b2d75-112">1. példa: Alkalmazás eltávolítása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="b2d75-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="b2d75-113">Eltávolítja a bérlői webhelyről a "b4cd1619-80b3-4cfb-9f8f-9f233425738" objektumazonosítójú alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b2d75-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="b2d75-114">2. példa: Alkalmazás eltávolítása alkalmazásazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="b2d75-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="b2d75-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlőből.</span><span class="sxs-lookup"><span data-stu-id="b2d75-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="b2d75-116">3. példa: Alkalmazás eltávolítása pipával</span><span class="sxs-lookup"><span data-stu-id="b2d75-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="b2d75-117">A (b4cd1619-80b3-4cfb-9f8f-9f233425738) objektumazonosítóval és a Remove-AzADApplication-parancsmaghoz az alkalmazás bérlői webhelyről való eltávolításához szükségescsövekkel együtt jut el az alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="b2d75-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="b2d75-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2d75-118">PARAMETERS</span></span>

### <span data-ttu-id="b2d75-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b2d75-119">-ApplicationId</span></span>
<span data-ttu-id="b2d75-120">Az eltávolítható alkalmazás alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b2d75-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d75-121">-DefaultProfile</span></span>
<span data-ttu-id="b2d75-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2d75-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2d75-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b2d75-123">-DisplayName</span></span>
<span data-ttu-id="b2d75-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="b2d75-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d75-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b2d75-125">-Force</span></span>
<span data-ttu-id="b2d75-126">Váltás alkalmazás törléséhez megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="b2d75-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="b2d75-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2d75-127">-InputObject</span></span>
<span data-ttu-id="b2d75-128">Az eltávolítható alkalmazást képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="b2d75-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d75-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b2d75-129">-ObjectId</span></span>
<span data-ttu-id="b2d75-130">A törölni kívánt alkalmazás objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b2d75-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d75-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2d75-131">-PassThru</span></span>
<span data-ttu-id="b2d75-132">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="b2d75-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b2d75-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2d75-133">-Confirm</span></span>
<span data-ttu-id="b2d75-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b2d75-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d75-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d75-135">-WhatIf</span></span>
<span data-ttu-id="b2d75-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2d75-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d75-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2d75-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d75-138">CommonParameters</span></span>
<span data-ttu-id="b2d75-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d75-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2d75-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d75-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2d75-141">INPUTS</span></span>

### <span data-ttu-id="b2d75-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b2d75-142">System.String</span></span>

### <span data-ttu-id="b2d75-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b2d75-143">System.Guid</span></span>

### <span data-ttu-id="b2d75-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b2d75-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b2d75-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2d75-145">OUTPUTS</span></span>

### <span data-ttu-id="b2d75-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2d75-146">System.Boolean</span></span>

## <span data-ttu-id="b2d75-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2d75-147">NOTES</span></span>
<span data-ttu-id="b2d75-148">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="b2d75-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b2d75-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2d75-149">RELATED LINKS</span></span>

[<span data-ttu-id="b2d75-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2d75-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b2d75-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2d75-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="b2d75-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2d75-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="b2d75-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b2d75-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

