---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: e9e4a8e902b3d71507a9e9d731ceb518825f8aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927793"
---
# <span data-ttu-id="947e5-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="947e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="947e5-102">SYNOPSIS</span></span>
<span data-ttu-id="947e5-103">Az Azure Active Directory szolgáltatásnév törlése.</span><span class="sxs-lookup"><span data-stu-id="947e5-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="947e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="947e5-104">SYNTAX</span></span>

### <span data-ttu-id="947e5-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="947e5-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e5-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e5-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e5-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e5-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e5-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e5-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e5-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e5-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947e5-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="947e5-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947e5-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="947e5-111">DESCRIPTION</span></span>
<span data-ttu-id="947e5-112">Az Azure Active Directory szolgáltatásnév törlése.</span><span class="sxs-lookup"><span data-stu-id="947e5-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="947e5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="947e5-113">EXAMPLES</span></span>

### <span data-ttu-id="947e5-114">1. példa : Egyszerű szolgáltatásnév eltávolítása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="947e5-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="947e5-115">A (61b5d8ea-fdc6-40a2-8d5b-ad447c678d45) objektumazonosítójú egyszerű szolgáltatásnév eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="947e5-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="947e5-116">2. példa : Egyszerű szolgáltatásnév eltávolítása alkalmazásazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="947e5-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="947e5-117">A (9263469e-d328-4321-8646-3e3e75d20e76) azonosítójú egyszerű szolgáltatásnév eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="947e5-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="947e5-118">3. példa: Egyszerű szolgáltatásnév eltávolítása SPN-ről</span><span class="sxs-lookup"><span data-stu-id="947e5-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="947e5-119">A szolgáltatásnév eltávolítása a "MyServicePrincipal" egyszerű szolgáltatásnévvel</span><span class="sxs-lookup"><span data-stu-id="947e5-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="947e5-120">4. példa : Egyszerű szolgáltatásnév eltávolítása pipázással</span><span class="sxs-lookup"><span data-stu-id="947e5-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="947e5-121">A (61b5d8ea-fdc6-40a2-8d5b-ad447c678d45) azonosítójú egyszerű szolgáltatásnév és a Remove-AzADServicePrincipal-parancsmagot a szolgáltatásnév eltávolításához vezető vezetékek segítségével.</span><span class="sxs-lookup"><span data-stu-id="947e5-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="947e5-122">5. példa: Egyszerű szolgáltatásnév eltávolítása egy alkalmazással</span><span class="sxs-lookup"><span data-stu-id="947e5-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="947e5-123">A (9263469e-d328-4321-8646-3e3e75d20e76) azonosítójú alkalmazást és az Remove-AzADServicePrincipal-parancsmaghoz tartozó, az adott alkalmazáshoz társított szolgáltatásnév eltávolításához szükségescsöveket használja.</span><span class="sxs-lookup"><span data-stu-id="947e5-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="947e5-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="947e5-124">PARAMETERS</span></span>

### <span data-ttu-id="947e5-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="947e5-125">-ApplicationId</span></span>
<span data-ttu-id="947e5-126">Az egyszerű szolgáltatásalkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="947e5-126">The service principal application id.</span></span>

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

### <span data-ttu-id="947e5-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="947e5-127">-ApplicationObject</span></span>
<span data-ttu-id="947e5-128">Az az alkalmazásobjektum, amelynek egyszerű szolgáltatását eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="947e5-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="947e5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947e5-129">-DefaultProfile</span></span>
<span data-ttu-id="947e5-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="947e5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="947e5-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="947e5-131">-DisplayName</span></span>
<span data-ttu-id="947e5-132">A szolgáltatásnév megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="947e5-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e5-133">-Force</span><span class="sxs-lookup"><span data-stu-id="947e5-133">-Force</span></span>
<span data-ttu-id="947e5-134">Váltás egyszerű szolgáltatásnév törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="947e5-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="947e5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="947e5-135">-InputObject</span></span>
<span data-ttu-id="947e5-136">A szolgáltatásnévobjektum.</span><span class="sxs-lookup"><span data-stu-id="947e5-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="947e5-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="947e5-137">-ObjectId</span></span>
<span data-ttu-id="947e5-138">A törölni kívánt szolgáltatásnév objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="947e5-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e5-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="947e5-139">-PassThru</span></span>
<span data-ttu-id="947e5-140">Ha meg van adva, akkor a törölt egyszerű szolgáltatásnév lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="947e5-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="947e5-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="947e5-141">-ServicePrincipalName</span></span>
<span data-ttu-id="947e5-142">A szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="947e5-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947e5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="947e5-143">-Confirm</span></span>
<span data-ttu-id="947e5-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="947e5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="947e5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947e5-145">-WhatIf</span></span>
<span data-ttu-id="947e5-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="947e5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="947e5-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="947e5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="947e5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947e5-148">CommonParameters</span></span>
<span data-ttu-id="947e5-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="947e5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947e5-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="947e5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947e5-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="947e5-151">INPUTS</span></span>

### <span data-ttu-id="947e5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="947e5-152">System.String</span></span>

### <span data-ttu-id="947e5-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="947e5-153">System.Guid</span></span>

### <span data-ttu-id="947e5-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="947e5-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="947e5-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="947e5-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="947e5-156">OUTPUTS</span></span>

### <span data-ttu-id="947e5-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="947e5-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="947e5-158">NOTES</span></span>
<span data-ttu-id="947e5-159">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="947e5-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="947e5-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="947e5-160">RELATED LINKS</span></span>

[<span data-ttu-id="947e5-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="947e5-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="947e5-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="947e5-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="947e5-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="947e5-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="947e5-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="947e5-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
