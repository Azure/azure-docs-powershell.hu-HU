---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/add-azureanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 39d15940b85e7da19cf4f8f23abee5db6223235f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492950"
---
# <span data-ttu-id="28bcf-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="28bcf-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="28bcf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="28bcf-103">Az Azure Analysis Services kiszolgálói parancsmag-kérelmekhez használt hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="28bcf-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28bcf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28bcf-104">SYNTAX</span></span>

### <span data-ttu-id="28bcf-105">UserParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28bcf-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28bcf-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="28bcf-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28bcf-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="28bcf-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28bcf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="28bcf-108">DESCRIPTION</span></span>
<span data-ttu-id="28bcf-109">A Add-AzureAnalysisServicesAccount parancsmag az Azure Analysis Services-kiszolgáló egy példányához való bejelentkezéskor használatos.</span><span class="sxs-lookup"><span data-stu-id="28bcf-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="28bcf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="28bcf-110">EXAMPLES</span></span>

### <span data-ttu-id="28bcf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28bcf-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="28bcf-112">Ebben a példában a $UserCredential változó által megadott fiókot fogja hozzáadni a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="28bcf-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="28bcf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="28bcf-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="28bcf-114">Az első parancs megkapja az Application Service Principal hitelesítő adatait, majd a $ApplicationCredential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="28bcf-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="28bcf-115">A második parancs hozzáadja a $ApplicationCredential változó és a bérlői azonosító megkeresése által megadott Application Service Principal-fiókot a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="28bcf-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="28bcf-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="28bcf-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="28bcf-117">Ebben a példában a ApplicationId, az bérlői azonosító megkeresése és a CertificateThumbprint által megadott Application Service Principal-fiókot fogja hozzáadni az westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="28bcf-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="28bcf-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28bcf-118">PARAMETERS</span></span>

### <span data-ttu-id="28bcf-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="28bcf-119">-ApplicationId</span></span>
<span data-ttu-id="28bcf-120">Az alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="28bcf-120">The application ID.</span></span>

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

### <span data-ttu-id="28bcf-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="28bcf-121">-CertificateThumbprint</span></span>
<span data-ttu-id="28bcf-122">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="28bcf-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="28bcf-123">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="28bcf-123">-Credential</span></span>
<span data-ttu-id="28bcf-124">Bejelentkezési hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="28bcf-124">Login credentials</span></span>

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

### <span data-ttu-id="28bcf-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="28bcf-125">-RolloutEnvironment</span></span>
<span data-ttu-id="28bcf-126">Annak az Azure Analysis Services-környezetnek a neve, amelybe be szeretne jelentkezni.</span><span class="sxs-lookup"><span data-stu-id="28bcf-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="28bcf-127">A kiszolgáló teljes neve (például asazure://westcentralus.asazure.windows.net/testserver) esetén a változó helyes értéke lesz westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="28bcf-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="28bcf-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="28bcf-128">-ServicePrincipal</span></span>
<span data-ttu-id="28bcf-129">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="28bcf-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="28bcf-130">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="28bcf-130">-TenantId</span></span>
<span data-ttu-id="28bcf-131">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="28bcf-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="28bcf-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28bcf-132">-Confirm</span></span>
<span data-ttu-id="28bcf-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28bcf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28bcf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28bcf-134">-WhatIf</span></span>
<span data-ttu-id="28bcf-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28bcf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28bcf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28bcf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28bcf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bcf-137">CommonParameters</span></span>
<span data-ttu-id="28bcf-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28bcf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bcf-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28bcf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bcf-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28bcf-140">INPUTS</span></span>

### <span data-ttu-id="28bcf-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="28bcf-141">None</span></span>

## <span data-ttu-id="28bcf-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28bcf-142">OUTPUTS</span></span>

### <span data-ttu-id="28bcf-143">Microsoft. Azure. Command. AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="28bcf-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="28bcf-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28bcf-144">NOTES</span></span>
<span data-ttu-id="28bcf-145">Alias: Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="28bcf-145">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="28bcf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28bcf-146">RELATED LINKS</span></span>
