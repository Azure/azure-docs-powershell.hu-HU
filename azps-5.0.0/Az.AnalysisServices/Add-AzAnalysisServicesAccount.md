---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296597"
---
# <span data-ttu-id="4c2f4-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4c2f4-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="4c2f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2f4-103">Az Azure Analysis Services kiszolgálói parancsmag-kérelmekhez használt hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="4c2f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c2f4-104">SYNTAX</span></span>

### <span data-ttu-id="4c2f4-105">UserParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c2f4-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c2f4-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4c2f4-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c2f4-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4c2f4-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c2f4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c2f4-108">DESCRIPTION</span></span>
<span data-ttu-id="4c2f4-109">A Add-AzAnalysisServicesAccount parancsmag az Azure Analysis Services-kiszolgáló egy példányához való bejelentkezéskor használatos.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="4c2f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c2f4-110">EXAMPLES</span></span>

### <span data-ttu-id="4c2f4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c2f4-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="4c2f4-112">Ebben a példában a $UserCredential változó által megadott fiókot fogja hozzáadni a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="4c2f4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c2f4-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="4c2f4-114">Az első parancs megkapja az Application Service Principal hitelesítő adatait, majd a $ApplicationCredential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="4c2f4-115">A második parancs hozzáadja a $ApplicationCredential változó és a bérlői azonosító megkeresése által megadott Application Service Principal-fiókot a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="4c2f4-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="4c2f4-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="4c2f4-117">Ebben a példában a ApplicationId, az bérlői azonosító megkeresése és a CertificateThumbprint által megadott Application Service Principal-fiókot fogja hozzáadni az westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="4c2f4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c2f4-118">PARAMETERS</span></span>

### <span data-ttu-id="4c2f4-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4c2f4-119">-ApplicationId</span></span>
<span data-ttu-id="4c2f4-120">Az alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-120">The application ID.</span></span>

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

### <span data-ttu-id="4c2f4-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4c2f4-121">-CertificateThumbprint</span></span>
<span data-ttu-id="4c2f4-122">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="4c2f4-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="4c2f4-123">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="4c2f4-123">-Credential</span></span>
<span data-ttu-id="4c2f4-124">Bejelentkezési hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="4c2f4-124">Login credentials</span></span>

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

### <span data-ttu-id="4c2f4-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="4c2f4-125">-RolloutEnvironment</span></span>
<span data-ttu-id="4c2f4-126">Annak az Azure Analysis Services-környezetnek a neve, amelybe be szeretne jelentkezni.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="4c2f4-127">A kiszolgáló teljes neve (például asazure://westcentralus.asazure.windows.net/testserver) esetén a változó helyes értéke lesz westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="4c2f4-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="4c2f4-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4c2f4-128">-ServicePrincipal</span></span>
<span data-ttu-id="4c2f4-129">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="4c2f4-130">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="4c2f4-130">-TenantId</span></span>
<span data-ttu-id="4c2f4-131">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="4c2f4-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="4c2f4-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c2f4-132">-Confirm</span></span>
<span data-ttu-id="4c2f4-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c2f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c2f4-134">-WhatIf</span></span>
<span data-ttu-id="4c2f4-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c2f4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c2f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2f4-137">CommonParameters</span></span>
<span data-ttu-id="4c2f4-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c2f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2f4-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c2f4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2f4-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c2f4-140">INPUTS</span></span>

### <span data-ttu-id="4c2f4-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="4c2f4-141">None</span></span>

## <span data-ttu-id="4c2f4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c2f4-142">OUTPUTS</span></span>

### <span data-ttu-id="4c2f4-143">Microsoft. Azure. Command. AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4c2f4-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="4c2f4-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c2f4-144">NOTES</span></span>
<span data-ttu-id="4c2f4-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="4c2f4-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="4c2f4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c2f4-146">RELATED LINKS</span></span>
