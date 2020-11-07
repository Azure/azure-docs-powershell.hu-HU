---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848093"
---
# <span data-ttu-id="d9f7c-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9f7c-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="d9f7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f7c-103">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="d9f7c-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9f7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9f7c-104">SYNTAX</span></span>

### <span data-ttu-id="d9f7c-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9f7c-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f7c-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7c-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f7c-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7c-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f7c-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f7c-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f7c-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9f7c-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f7c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9f7c-111">DESCRIPTION</span></span>
<span data-ttu-id="d9f7c-112">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="d9f7c-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="d9f7c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d9f7c-113">EXAMPLES</span></span>

### <span data-ttu-id="d9f7c-114">Példa 1 – objektumazonosítók eltávolítása objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="d9f7c-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="d9f7c-115">Eltávolítja a "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="d9f7c-116">2. példa – a szolgáltatás megbízójának eltávolítása alkalmazás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="d9f7c-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="d9f7c-117">Eltávolítja a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="d9f7c-118">3 példa – egy egyszerű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9f7c-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="d9f7c-119">A Service Principal "MyServicePrincipal" nevű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9f7c-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="d9f7c-120">4. példa – a szolgáltatási tőkeösszeg eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d9f7c-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="d9f7c-121">A "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet és az Remove-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket kapja meg, így eltávolítja a szolgáltatást a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="d9f7c-122">Példa: 5 – a szolgáltatásnév eltávolítása egy alkalmazással</span><span class="sxs-lookup"><span data-stu-id="d9f7c-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="d9f7c-123">Beilleszti az alkalmazást a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú alkalmazás-azonosítóval, és a Remove-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket az alkalmazáshoz társított szolgáltató eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="d9f7c-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9f7c-124">PARAMETERS</span></span>

### <span data-ttu-id="d9f7c-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d9f7c-125">-ApplicationId</span></span>
<span data-ttu-id="d9f7c-126">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-126">The service principal application id.</span></span>

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

### <span data-ttu-id="d9f7c-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d9f7c-127">-ApplicationObject</span></span>
<span data-ttu-id="d9f7c-128">Annak az alkalmazásobjektum-objektumnak a törlése, amelynek a szolgáltatását el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f7c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f7c-129">-DefaultProfile</span></span>
<span data-ttu-id="d9f7c-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9f7c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9f7c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9f7c-131">-DisplayName</span></span>
<span data-ttu-id="d9f7c-132">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="d9f7c-133">-Force</span><span class="sxs-lookup"><span data-stu-id="d9f7c-133">-Force</span></span>
<span data-ttu-id="d9f7c-134">Váltás a szolgáltatás megbízójának törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="d9f7c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f7c-135">-InputObject</span></span>
<span data-ttu-id="d9f7c-136">A Service Principal objektum.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f7c-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9f7c-137">-ObjectId</span></span>
<span data-ttu-id="d9f7c-138">A törlendő szolgáltató objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f7c-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9f7c-139">-PassThru</span></span>
<span data-ttu-id="d9f7c-140">Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="d9f7c-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9f7c-141">-ServicePrincipalName</span></span>
<span data-ttu-id="d9f7c-142">A szolgáltatás egyszerű neve.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-142">The service principal name.</span></span>

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

### <span data-ttu-id="d9f7c-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9f7c-143">-Confirm</span></span>
<span data-ttu-id="d9f7c-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f7c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f7c-145">-WhatIf</span></span>
<span data-ttu-id="d9f7c-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f7c-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9f7c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f7c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f7c-148">CommonParameters</span></span>
<span data-ttu-id="d9f7c-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9f7c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f7c-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f7c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f7c-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9f7c-151">INPUTS</span></span>

### <span data-ttu-id="d9f7c-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9f7c-152">System.Guid</span></span>

### <span data-ttu-id="d9f7c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d9f7c-153">System.String</span></span>

### <span data-ttu-id="d9f7c-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9f7c-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="d9f7c-155">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9f7c-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d9f7c-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d9f7c-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="d9f7c-157">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9f7c-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="d9f7c-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9f7c-158">OUTPUTS</span></span>

### <span data-ttu-id="d9f7c-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9f7c-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="d9f7c-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9f7c-160">NOTES</span></span>
<span data-ttu-id="d9f7c-161">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="d9f7c-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d9f7c-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9f7c-162">RELATED LINKS</span></span>

[<span data-ttu-id="d9f7c-163">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9f7c-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d9f7c-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d9f7c-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="d9f7c-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d9f7c-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="d9f7c-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d9f7c-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
