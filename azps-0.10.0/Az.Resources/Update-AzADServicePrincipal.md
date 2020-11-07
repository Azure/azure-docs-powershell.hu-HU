---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e2c8e8fea9f8f86f06a9808158c50cb63915106b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843145"
---
# <span data-ttu-id="ec45c-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ec45c-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="ec45c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec45c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec45c-103">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="ec45c-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="ec45c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec45c-104">SYNTAX</span></span>

### <span data-ttu-id="ec45c-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec45c-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec45c-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec45c-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec45c-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec45c-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec45c-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec45c-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec45c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec45c-109">DESCRIPTION</span></span>
<span data-ttu-id="ec45c-110">Frissít egy meglévő Azure Active Directory-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="ec45c-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="ec45c-111">Ha frissíteni szeretné az ehhez a szolgáltatáshoz tartozó hitelesítő adatokat, használja az New-AzADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ec45c-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="ec45c-112">Ha frissíteni szeretné a mögöttes alkalmazáshoz tartozó tulajdonságokat, használja az Update-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ec45c-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="ec45c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ec45c-113">EXAMPLES</span></span>

### <span data-ttu-id="ec45c-114">Példa 1 – egy egyszerű szolgáltatásnév megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="ec45c-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="ec45c-115">Frissíti a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú, "MyNewDisplayName" azonosítójú szolgáltatásnév megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="ec45c-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ec45c-116">2 – példa – egy egyszerű szolgáltatásnév megjelenítési nevének frissítése a csövekkel</span><span class="sxs-lookup"><span data-stu-id="ec45c-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="ec45c-117">Megkapja a "784136ca-3ae2-4fdd-a388-89d793e7c780" azonosítójú szolgáltatásnevet, valamint az Update-AzADServicePrincipal parancsmagot tartalmazó csöveket, így a szolgáltatás nevének neve a "MyNewDisplayName" névre frissíthető.</span><span class="sxs-lookup"><span data-stu-id="ec45c-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="ec45c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec45c-118">PARAMETERS</span></span>

### <span data-ttu-id="ec45c-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec45c-119">-ApplicationId</span></span>
<span data-ttu-id="ec45c-120">A frissítendő szolgáltatásnevet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec45c-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="ec45c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec45c-121">-DefaultProfile</span></span>
<span data-ttu-id="ec45c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec45c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec45c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec45c-123">-DisplayName</span></span>
<span data-ttu-id="ec45c-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="ec45c-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="ec45c-125">-Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="ec45c-125">-Homepage</span></span>
<span data-ttu-id="ec45c-126">A szolgáltatás fő weboldala.</span><span class="sxs-lookup"><span data-stu-id="ec45c-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="ec45c-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="ec45c-127">-IdentifierUri</span></span>
<span data-ttu-id="ec45c-128">A szolgáltatásnevet azonosító URI (ok).</span><span class="sxs-lookup"><span data-stu-id="ec45c-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="ec45c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec45c-129">-InputObject</span></span>
<span data-ttu-id="ec45c-130">A frissítendő szolgáltatásnevet képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="ec45c-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="ec45c-131">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ec45c-131">-KeyCredential</span></span>
<span data-ttu-id="ec45c-132">A fő hitelesítő adatok a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="ec45c-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="ec45c-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec45c-133">-ObjectId</span></span>
<span data-ttu-id="ec45c-134">A frissítendő szolgáltatásnevet azonosító.</span><span class="sxs-lookup"><span data-stu-id="ec45c-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="ec45c-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="ec45c-135">-PasswordCredential</span></span>
<span data-ttu-id="ec45c-136">A szolgáltatóhoz tartozó jelszó (ok) a hitelesítő adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="ec45c-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="ec45c-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ec45c-137">-ServicePrincipalName</span></span>
<span data-ttu-id="ec45c-138">A frissítendő szolgáltatásnév.</span><span class="sxs-lookup"><span data-stu-id="ec45c-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="ec45c-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec45c-139">-Confirm</span></span>
<span data-ttu-id="ec45c-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec45c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec45c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec45c-141">-WhatIf</span></span>
<span data-ttu-id="ec45c-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec45c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec45c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec45c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec45c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec45c-144">CommonParameters</span></span>
<span data-ttu-id="ec45c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec45c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec45c-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec45c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec45c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec45c-147">INPUTS</span></span>

### <span data-ttu-id="ec45c-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ec45c-148">System.Guid</span></span>

### <span data-ttu-id="ec45c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ec45c-149">System.String</span></span>

### <span data-ttu-id="ec45c-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ec45c-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="ec45c-151">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ec45c-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ec45c-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec45c-152">OUTPUTS</span></span>

### <span data-ttu-id="ec45c-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ec45c-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ec45c-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec45c-154">NOTES</span></span>

## <span data-ttu-id="ec45c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec45c-155">RELATED LINKS</span></span>
