---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325524"
---
# <span data-ttu-id="c5b0e-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c5b0e-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="c5b0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b0e-103">Egy meglévő Azure Active Directory-szolgáltatásnév frissítése.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="c5b0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5b0e-104">SYNTAX</span></span>

### <span data-ttu-id="c5b0e-105">SpObjectIdWithDisplayNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5b0e-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b0e-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b0e-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b0e-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b0e-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5b0e-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5b0e-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b0e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5b0e-109">DESCRIPTION</span></span>
<span data-ttu-id="c5b0e-110">Egy meglévő Azure Active Directory-szolgáltatásnév frissítése.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c5b0e-111">A szolgáltatásnévvel társított hitelesítő adatok frissítéséhez használja a New-AzADSpCredential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="c5b0e-112">Az alapul szolgáló alkalmazás tulajdonságainak frissítéséhez használja az Update-AzADApplication parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="c5b0e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5b0e-113">EXAMPLES</span></span>

### <span data-ttu-id="c5b0e-114">1. példa: Egyszerű szolgáltatásnév megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="c5b0e-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c5b0e-115">Frissíti a szolgáltatásnév megjelenítendő nevét a (784136ca-3ae2-4fdd-a388-89d793e7c780) azonosítóval "MyNewDisplayName" azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c5b0e-116">2. példa: Egyszerű szolgáltatásnév megjelenítendő nevének frissítése pipázással</span><span class="sxs-lookup"><span data-stu-id="c5b0e-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="c5b0e-117">A (784136ca-3ae2-4fdd-a388-89d793e7c780) azonosítójú egyszerű szolgáltatásnevet, valamint a Update-AzADServicePrincipal-parancsmagot a "MyNewDisplayName" megjelenítési nevének frissítéséhez a Update-AzADServicePrincipal-parancsmaghoz vezető vezetékneveket kapja.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="c5b0e-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="c5b0e-118">Example 3</span></span>

<span data-ttu-id="c5b0e-119">Egy meglévő Azure Active Directory-szolgáltatásnév frissítése.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c5b0e-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="c5b0e-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="c5b0e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5b0e-121">PARAMETERS</span></span>

### <span data-ttu-id="c5b0e-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c5b0e-122">-ApplicationId</span></span>
<span data-ttu-id="c5b0e-123">A frissíteni szükséges egyszerű szolgáltatásnév alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="c5b0e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b0e-124">-DefaultProfile</span></span>
<span data-ttu-id="c5b0e-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b0e-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5b0e-126">-DisplayName</span></span>
<span data-ttu-id="c5b0e-127">A szolgáltatásnév megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="c5b0e-128">- Kezdőlap</span><span class="sxs-lookup"><span data-stu-id="c5b0e-128">-Homepage</span></span>
<span data-ttu-id="c5b0e-129">A szolgáltatásnév kezdőlapja.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="c5b0e-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c5b0e-130">-IdentifierUri</span></span>
<span data-ttu-id="c5b0e-131">A szolgáltatásnév azonosító URI-ját.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="c5b0e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5b0e-132">-InputObject</span></span>
<span data-ttu-id="c5b0e-133">A frissítend kell a szolgáltatásnévnek megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="c5b0e-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c5b0e-134">-KeyCredential</span></span>
<span data-ttu-id="c5b0e-135">A szolgáltatásnév kulcs hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c5b0e-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c5b0e-136">-ObjectId</span></span>
<span data-ttu-id="c5b0e-137">A frissítend kell a szolgáltatásnév objektumazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="c5b0e-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c5b0e-138">-PasswordCredential</span></span>
<span data-ttu-id="c5b0e-139">A szolgáltatásnévhez használt jelszó hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c5b0e-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c5b0e-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c5b0e-141">A frissítend kell a egyszerű szolgáltatásnév SPN-ét.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="c5b0e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5b0e-142">-Confirm</span></span>
<span data-ttu-id="c5b0e-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b0e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b0e-144">-WhatIf</span></span>
<span data-ttu-id="c5b0e-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b0e-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b0e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b0e-147">CommonParameters</span></span>
<span data-ttu-id="c5b0e-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b0e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b0e-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5b0e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b0e-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5b0e-150">INPUTS</span></span>

### <span data-ttu-id="c5b0e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c5b0e-151">System.String</span></span>

### <span data-ttu-id="c5b0e-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c5b0e-152">System.Guid</span></span>

### <span data-ttu-id="c5b0e-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c5b0e-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c5b0e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5b0e-154">OUTPUTS</span></span>

### <span data-ttu-id="c5b0e-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c5b0e-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c5b0e-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5b0e-156">NOTES</span></span>

## <span data-ttu-id="c5b0e-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5b0e-157">RELATED LINKS</span></span>