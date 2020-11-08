---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 7f306503754ca945ab4abb001cf08f8574b67025
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185886"
---
# <span data-ttu-id="4655f-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="4655f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4655f-102">SYNOPSIS</span></span>
<span data-ttu-id="4655f-103">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="4655f-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="4655f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4655f-104">SYNTAX</span></span>

### <span data-ttu-id="4655f-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4655f-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4655f-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="4655f-111">DESCRIPTION</span></span>
<span data-ttu-id="4655f-112">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="4655f-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="4655f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4655f-113">EXAMPLES</span></span>

### <span data-ttu-id="4655f-114">Példa 1 – objektumazonosítók eltávolítása objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="4655f-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="4655f-115">Eltávolítja a "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="4655f-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="4655f-116">2. példa – a szolgáltatás megbízójának eltávolítása alkalmazás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="4655f-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="4655f-117">Eltávolítja a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="4655f-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="4655f-118">3 példa – egy egyszerű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4655f-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="4655f-119">A Service Principal "MyServicePrincipal" nevű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4655f-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="4655f-120">4. példa – a szolgáltatási tőkeösszeg eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4655f-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="4655f-121">A "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet és az Remove-AzADServicePrincipal parancsmagot tartalmazó csöveket kapja meg, így eltávolítja a szolgáltatást a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="4655f-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="4655f-122">Példa: 5 – a szolgáltatásnév eltávolítása egy alkalmazással</span><span class="sxs-lookup"><span data-stu-id="4655f-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="4655f-123">Beilleszti az alkalmazást a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú alkalmazás-azonosítóval, és a Remove-AzADServicePrincipal parancsmagot tartalmazó csöveket az alkalmazáshoz társított szolgáltató eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="4655f-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="4655f-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4655f-124">PARAMETERS</span></span>

### <span data-ttu-id="4655f-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4655f-125">-ApplicationId</span></span>
<span data-ttu-id="4655f-126">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="4655f-126">The service principal application id.</span></span>

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

### <span data-ttu-id="4655f-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4655f-127">-ApplicationObject</span></span>
<span data-ttu-id="4655f-128">Annak az alkalmazásobjektum-objektumnak a törlése, amelynek a szolgáltatását el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="4655f-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="4655f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4655f-129">-DefaultProfile</span></span>
<span data-ttu-id="4655f-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4655f-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4655f-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4655f-131">-DisplayName</span></span>
<span data-ttu-id="4655f-132">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="4655f-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="4655f-133">-Force</span><span class="sxs-lookup"><span data-stu-id="4655f-133">-Force</span></span>
<span data-ttu-id="4655f-134">Váltás a szolgáltatás megbízójának törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="4655f-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="4655f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4655f-135">-InputObject</span></span>
<span data-ttu-id="4655f-136">A Service Principal objektum.</span><span class="sxs-lookup"><span data-stu-id="4655f-136">The service principal object.</span></span>

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

### <span data-ttu-id="4655f-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4655f-137">-ObjectId</span></span>
<span data-ttu-id="4655f-138">A törlendő szolgáltató objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4655f-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="4655f-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4655f-139">-PassThru</span></span>
<span data-ttu-id="4655f-140">Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4655f-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="4655f-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4655f-141">-ServicePrincipalName</span></span>
<span data-ttu-id="4655f-142">A szolgáltatás egyszerű neve.</span><span class="sxs-lookup"><span data-stu-id="4655f-142">The service principal name.</span></span>

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

### <span data-ttu-id="4655f-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4655f-143">-Confirm</span></span>
<span data-ttu-id="4655f-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4655f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4655f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4655f-145">-WhatIf</span></span>
<span data-ttu-id="4655f-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4655f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4655f-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4655f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4655f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4655f-148">CommonParameters</span></span>
<span data-ttu-id="4655f-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4655f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4655f-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4655f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4655f-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4655f-151">INPUTS</span></span>

### <span data-ttu-id="4655f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4655f-152">System.String</span></span>

### <span data-ttu-id="4655f-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4655f-153">System.Guid</span></span>

### <span data-ttu-id="4655f-154">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="4655f-155">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4655f-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="4655f-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4655f-156">OUTPUTS</span></span>

### <span data-ttu-id="4655f-157">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4655f-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4655f-158">NOTES</span></span>
<span data-ttu-id="4655f-159">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="4655f-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4655f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4655f-160">RELATED LINKS</span></span>

[<span data-ttu-id="4655f-161">Új – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="4655f-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="4655f-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4655f-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="4655f-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4655f-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="4655f-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4655f-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)