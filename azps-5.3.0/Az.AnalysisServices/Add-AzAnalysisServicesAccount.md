---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479098"
---
# <span data-ttu-id="67033-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="67033-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="67033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67033-102">SYNOPSIS</span></span>
<span data-ttu-id="67033-103">Egy hitelesített fiókot ad hozzá az Azure Analysis Services-kiszolgálói parancsmagkéréshez.</span><span class="sxs-lookup"><span data-stu-id="67033-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="67033-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67033-104">SYNTAX</span></span>

### <span data-ttu-id="67033-105">UserParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67033-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67033-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="67033-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67033-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="67033-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67033-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67033-108">DESCRIPTION</span></span>
<span data-ttu-id="67033-109">A Add-AzAnalysisServicesAccount parancsmag használatával lehet bejelentkezni az Azure Analysis Services-kiszolgáló egy példányába</span><span class="sxs-lookup"><span data-stu-id="67033-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="67033-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67033-110">EXAMPLES</span></span>

### <span data-ttu-id="67033-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="67033-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="67033-112">Ez a példa hozzáadja a $UserCredential által megadott fiókot az westcentralus.asazure.windows.net Analysis Services környezethez.</span><span class="sxs-lookup"><span data-stu-id="67033-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="67033-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="67033-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="67033-114">Az első parancs az alkalmazás egyszerű szolgáltatásának hitelesítő adatait kapja meg, majd tárolja őket a $ApplicationCredential változóban.</span><span class="sxs-lookup"><span data-stu-id="67033-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="67033-115">A második parancs hozzáadja a $ApplicationCredential és TenantId változó által megadott egyszerű alkalmazásszolgáltatás-fiókot a westcentralus.asazure.windows.net Analysis Services környezethez.</span><span class="sxs-lookup"><span data-stu-id="67033-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="67033-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="67033-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="67033-117">Ebben a példában az ApplicationId, a TenantId és a CertificateThumbprint által megadott egyszerű alkalmazásszolgáltatás-fiókot adjuk hozzá az westcentralus.asazure.windows.net Analysis Services környezethez.</span><span class="sxs-lookup"><span data-stu-id="67033-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="67033-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67033-118">PARAMETERS</span></span>

### <span data-ttu-id="67033-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67033-119">-ApplicationId</span></span>
<span data-ttu-id="67033-120">Az alkalmazásazonosító.</span><span class="sxs-lookup"><span data-stu-id="67033-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="67033-121">-CertificateThumbprint</span></span>
<span data-ttu-id="67033-122">Tanúsítvány kivonata (thumbprint)</span><span class="sxs-lookup"><span data-stu-id="67033-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-123">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="67033-123">-Credential</span></span>
<span data-ttu-id="67033-124">Bejelentkezési hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="67033-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="67033-125">-RolloutEnvironment</span></span>
<span data-ttu-id="67033-126">Annak az Azure Analysis Services-környezetnek a neve, amelybe be kell jelentkeznie.</span><span class="sxs-lookup"><span data-stu-id="67033-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="67033-127">A kiszolgáló teljes nevét (például asazure://westcentralus.asazure.windows.net/testserver) megadva a változó helyes értéke lesz westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="67033-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="67033-128">-ServicePrincipal</span></span>
<span data-ttu-id="67033-129">Azt jelzi, hogy a fiók hitelesítése egyszerű szolgáltatásnévvel megadott hitelesítő adatokkal történik.</span><span class="sxs-lookup"><span data-stu-id="67033-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="67033-130">-TenantId</span></span>
<span data-ttu-id="67033-131">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="67033-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67033-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67033-132">-Confirm</span></span>
<span data-ttu-id="67033-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="67033-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67033-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67033-134">-WhatIf</span></span>
<span data-ttu-id="67033-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="67033-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67033-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67033-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67033-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67033-137">CommonParameters</span></span>
<span data-ttu-id="67033-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67033-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67033-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67033-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67033-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67033-140">INPUTS</span></span>

### <span data-ttu-id="67033-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="67033-141">None</span></span>

## <span data-ttu-id="67033-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67033-142">OUTPUTS</span></span>

### <span data-ttu-id="67033-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="67033-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="67033-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67033-144">NOTES</span></span>
<span data-ttu-id="67033-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="67033-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="67033-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67033-146">RELATED LINKS</span></span>
