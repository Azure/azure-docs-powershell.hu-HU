---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 07bc19bd2314164b37ec9e014f5cad68de97d21f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494944"
---
# <span data-ttu-id="a3b09-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="a3b09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b09-103">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="a3b09-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3b09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3b09-104">SYNTAX</span></span>

### <span data-ttu-id="a3b09-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3b09-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b09-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3b09-111">DESCRIPTION</span></span>
<span data-ttu-id="a3b09-112">Az Azure Active Directory Service Principal törlése</span><span class="sxs-lookup"><span data-stu-id="a3b09-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="a3b09-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a3b09-113">EXAMPLES</span></span>

### <span data-ttu-id="a3b09-114">Példa 1 – objektumazonosítók eltávolítása objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a3b09-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="a3b09-115">Eltávolítja a "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="a3b09-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="a3b09-116">2. példa – a szolgáltatás megbízójának eltávolítása alkalmazás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a3b09-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="a3b09-117">Eltávolítja a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú szolgáltatásnevet.</span><span class="sxs-lookup"><span data-stu-id="a3b09-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="a3b09-118">3 példa – egy egyszerű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3b09-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="a3b09-119">A Service Principal "MyServicePrincipal" nevű szolgáltatásnév eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3b09-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="a3b09-120">4. példa – a szolgáltatási tőkeösszeg eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a3b09-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="a3b09-121">A "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" azonosítójú szolgáltatásnevet és az Remove-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket kapja meg, így eltávolítja a szolgáltatást a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="a3b09-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="a3b09-122">Példa: 5 – a szolgáltatásnév eltávolítása egy alkalmazással</span><span class="sxs-lookup"><span data-stu-id="a3b09-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="a3b09-123">Beilleszti az alkalmazást a "9263469e-d328-4321-8646-3e3e75d20e76" azonosítójú alkalmazás-azonosítóval, és a Remove-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket az alkalmazáshoz társított szolgáltató eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="a3b09-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="a3b09-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3b09-124">PARAMETERS</span></span>

### <span data-ttu-id="a3b09-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a3b09-125">-ApplicationId</span></span>
<span data-ttu-id="a3b09-126">A Service Principal Application azonosító.</span><span class="sxs-lookup"><span data-stu-id="a3b09-126">The service principal application id.</span></span>

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

### <span data-ttu-id="a3b09-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a3b09-127">-ApplicationObject</span></span>
<span data-ttu-id="a3b09-128">Annak az alkalmazásobjektum-objektumnak a törlése, amelynek a szolgáltatását el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="a3b09-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="a3b09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b09-129">-DefaultProfile</span></span>
<span data-ttu-id="a3b09-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3b09-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b09-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3b09-131">-DisplayName</span></span>
<span data-ttu-id="a3b09-132">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="a3b09-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="a3b09-133">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b09-133">-Force</span></span>
<span data-ttu-id="a3b09-134">Váltás a szolgáltatás megbízójának törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="a3b09-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="a3b09-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3b09-135">-InputObject</span></span>
<span data-ttu-id="a3b09-136">A Service Principal objektum.</span><span class="sxs-lookup"><span data-stu-id="a3b09-136">The service principal object.</span></span>

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

### <span data-ttu-id="a3b09-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a3b09-137">-ObjectId</span></span>
<span data-ttu-id="a3b09-138">A törlendő szolgáltató objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3b09-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="a3b09-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3b09-139">-PassThru</span></span>
<span data-ttu-id="a3b09-140">Ha meg van adva, akkor a törölt szolgáltatási megbízót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a3b09-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="a3b09-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a3b09-141">-ServicePrincipalName</span></span>
<span data-ttu-id="a3b09-142">A szolgáltatás egyszerű neve.</span><span class="sxs-lookup"><span data-stu-id="a3b09-142">The service principal name.</span></span>

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

### <span data-ttu-id="a3b09-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3b09-143">-Confirm</span></span>
<span data-ttu-id="a3b09-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3b09-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b09-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b09-145">-WhatIf</span></span>
<span data-ttu-id="a3b09-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3b09-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b09-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3b09-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b09-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b09-148">CommonParameters</span></span>
<span data-ttu-id="a3b09-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3b09-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b09-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b09-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b09-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b09-151">INPUTS</span></span>

### <span data-ttu-id="a3b09-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a3b09-152">System.Guid</span></span>

### <span data-ttu-id="a3b09-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b09-153">System.String</span></span>

### <span data-ttu-id="a3b09-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="a3b09-155">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3b09-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a3b09-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a3b09-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="a3b09-157">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3b09-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="a3b09-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b09-158">OUTPUTS</span></span>

### <span data-ttu-id="a3b09-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a3b09-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3b09-160">NOTES</span></span>
<span data-ttu-id="a3b09-161">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="a3b09-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a3b09-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3b09-162">RELATED LINKS</span></span>

[<span data-ttu-id="a3b09-163">Új – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a3b09-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a3b09-165">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a3b09-165">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="a3b09-166">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a3b09-166">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="a3b09-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a3b09-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
