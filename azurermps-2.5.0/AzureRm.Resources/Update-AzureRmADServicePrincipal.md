---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: d3e5459c81d2abbe7178652ce7b00fc35e6e3bbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849018"
---
# <span data-ttu-id="63a99-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63a99-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="63a99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63a99-102">SYNOPSIS</span></span>
<span data-ttu-id="63a99-103">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="63a99-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63a99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63a99-104">SYNTAX</span></span>

### <span data-ttu-id="63a99-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63a99-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a99-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a99-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a99-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a99-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a99-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a99-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63a99-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="63a99-109">DESCRIPTION</span></span>
<span data-ttu-id="63a99-110">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="63a99-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="63a99-111">Ha frissíteni szeretné az ehhez a szolgáltatáshoz tartozó hitelesítő adatokat, használja az New-AzureRmADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="63a99-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="63a99-112">Ha frissíteni szeretné a mögöttes alkalmazáshoz tartozó tulajdonságokat, használja az Update-AzureRmADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="63a99-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="63a99-113">Példák</span><span class="sxs-lookup"><span data-stu-id="63a99-113">EXAMPLES</span></span>

### <span data-ttu-id="63a99-114">Példa 1 – egy egyszerű szolgáltatásnév megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="63a99-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="63a99-115">Frissíti a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú, "MyNewDisplayName" azonosítójú szolgáltatásnév megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="63a99-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="63a99-116">2 – példa – egy egyszerű szolgáltatásnév megjelenítési nevének frissítése a csövekkel</span><span class="sxs-lookup"><span data-stu-id="63a99-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="63a99-117">Megkapja a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú szolgáltatásnevet, valamint az Update-AzureRmADServicePrincipal parancsmagot tartalmazó csöveket, így a szolgáltatás nevének neve a "MyNewDisplayName" névre frissíthető.</span><span class="sxs-lookup"><span data-stu-id="63a99-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="63a99-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63a99-118">PARAMETERS</span></span>

### <span data-ttu-id="63a99-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="63a99-119">-ApplicationId</span></span>
<span data-ttu-id="63a99-120">A frissítendő szolgáltatásnevet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="63a99-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a99-121">-DefaultProfile</span></span>
<span data-ttu-id="63a99-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63a99-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a99-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63a99-123">-DisplayName</span></span>
<span data-ttu-id="63a99-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="63a99-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-125">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="63a99-125">-Homepage</span></span>
<span data-ttu-id="63a99-126">A szolgáltatás fő weboldala.</span><span class="sxs-lookup"><span data-stu-id="63a99-126">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="63a99-127">-IdentifierUri</span></span>
<span data-ttu-id="63a99-128">A szolgáltatásnevet azonosító URI (ok).</span><span class="sxs-lookup"><span data-stu-id="63a99-128">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63a99-129">-InputObject</span></span>
<span data-ttu-id="63a99-130">A frissítendő szolgáltatásnevet képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="63a99-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-131">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="63a99-131">-KeyCredential</span></span>
<span data-ttu-id="63a99-132">A fő hitelesítő adatok a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="63a99-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="63a99-133">-ObjectId</span></span>
<span data-ttu-id="63a99-134">A frissítendő szolgáltatásnevet azonosító.</span><span class="sxs-lookup"><span data-stu-id="63a99-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="63a99-135">-PasswordCredential</span></span>
<span data-ttu-id="63a99-136">A szolgáltatóhoz tartozó jelszó (ok) a hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="63a99-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="63a99-137">-ServicePrincipalName</span></span>
<span data-ttu-id="63a99-138">A frissítendő szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="63a99-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a99-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63a99-139">-Confirm</span></span>
<span data-ttu-id="63a99-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63a99-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a99-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a99-141">-WhatIf</span></span>
<span data-ttu-id="63a99-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63a99-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a99-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63a99-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a99-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a99-144">CommonParameters</span></span>
<span data-ttu-id="63a99-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63a99-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a99-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a99-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a99-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a99-147">INPUTS</span></span>

### <span data-ttu-id="63a99-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="63a99-148">System.Guid</span></span>

### <span data-ttu-id="63a99-149">System. String</span><span class="sxs-lookup"><span data-stu-id="63a99-149">System.String</span></span>

### <span data-ttu-id="63a99-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63a99-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="63a99-151">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63a99-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="63a99-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a99-152">OUTPUTS</span></span>

### <span data-ttu-id="63a99-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63a99-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="63a99-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63a99-154">NOTES</span></span>

## <span data-ttu-id="63a99-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63a99-155">RELATED LINKS</span></span>
