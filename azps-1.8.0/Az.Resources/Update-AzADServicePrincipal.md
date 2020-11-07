---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e4fafb6c1ddc4dda05b6536501f713d04c312172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669292"
---
# <span data-ttu-id="e05f0-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e05f0-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="e05f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e05f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e05f0-103">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="e05f0-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="e05f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e05f0-104">SYNTAX</span></span>

### <span data-ttu-id="e05f0-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e05f0-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05f0-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05f0-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05f0-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05f0-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05f0-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05f0-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05f0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e05f0-109">DESCRIPTION</span></span>
<span data-ttu-id="e05f0-110">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="e05f0-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="e05f0-111">Ha frissíteni szeretné az ehhez a szolgáltatáshoz tartozó hitelesítő adatokat, használja az New-AzADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e05f0-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="e05f0-112">Ha frissíteni szeretné a mögöttes alkalmazáshoz tartozó tulajdonságokat, használja az Update-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e05f0-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="e05f0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e05f0-113">EXAMPLES</span></span>

### <span data-ttu-id="e05f0-114">Példa 1 – egy egyszerű szolgáltatásnév megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="e05f0-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e05f0-115">Frissíti a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú, "MyNewDisplayName" azonosítójú szolgáltatásnév megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="e05f0-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e05f0-116">2 – példa – egy egyszerű szolgáltatásnév megjelenítési nevének frissítése a csövekkel</span><span class="sxs-lookup"><span data-stu-id="e05f0-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="e05f0-117">Megkapja a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú szolgáltatásnevet, valamint az Update-AzADServicePrincipal parancsmagot tartalmazó csöveket, így a szolgáltatás nevének neve a "MyNewDisplayName" névre frissíthető.</span><span class="sxs-lookup"><span data-stu-id="e05f0-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="e05f0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e05f0-118">PARAMETERS</span></span>

### <span data-ttu-id="e05f0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e05f0-119">-ApplicationId</span></span>
<span data-ttu-id="e05f0-120">A frissítendő szolgáltatásnevet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e05f0-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="e05f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05f0-121">-DefaultProfile</span></span>
<span data-ttu-id="e05f0-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e05f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05f0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e05f0-123">-DisplayName</span></span>
<span data-ttu-id="e05f0-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="e05f0-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="e05f0-125">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="e05f0-125">-Homepage</span></span>
<span data-ttu-id="e05f0-126">A szolgáltatás fő weboldala.</span><span class="sxs-lookup"><span data-stu-id="e05f0-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="e05f0-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e05f0-127">-IdentifierUri</span></span>
<span data-ttu-id="e05f0-128">A szolgáltatásnevet azonosító URI (ok).</span><span class="sxs-lookup"><span data-stu-id="e05f0-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="e05f0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e05f0-129">-InputObject</span></span>
<span data-ttu-id="e05f0-130">A frissítendő szolgáltatásnevet képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="e05f0-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05f0-131">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="e05f0-131">-KeyCredential</span></span>
<span data-ttu-id="e05f0-132">A fő hitelesítő adatok a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="e05f0-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05f0-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e05f0-133">-ObjectId</span></span>
<span data-ttu-id="e05f0-134">A frissítendő szolgáltatásnevet azonosító.</span><span class="sxs-lookup"><span data-stu-id="e05f0-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05f0-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="e05f0-135">-PasswordCredential</span></span>
<span data-ttu-id="e05f0-136">A szolgáltatóhoz tartozó jelszó (ok) a hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="e05f0-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05f0-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e05f0-137">-ServicePrincipalName</span></span>
<span data-ttu-id="e05f0-138">A frissítendő szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="e05f0-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="e05f0-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e05f0-139">-Confirm</span></span>
<span data-ttu-id="e05f0-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e05f0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05f0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05f0-141">-WhatIf</span></span>
<span data-ttu-id="e05f0-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e05f0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05f0-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e05f0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05f0-144">CommonParameters</span></span>
<span data-ttu-id="e05f0-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e05f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05f0-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05f0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05f0-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e05f0-147">INPUTS</span></span>

### <span data-ttu-id="e05f0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e05f0-148">System.String</span></span>

### <span data-ttu-id="e05f0-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e05f0-149">System.Guid</span></span>

### <span data-ttu-id="e05f0-150">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e05f0-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e05f0-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e05f0-151">OUTPUTS</span></span>

### <span data-ttu-id="e05f0-152">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e05f0-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e05f0-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e05f0-153">NOTES</span></span>

## <span data-ttu-id="e05f0-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e05f0-154">RELATED LINKS</span></span>
