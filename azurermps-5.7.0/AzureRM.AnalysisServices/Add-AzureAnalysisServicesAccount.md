---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/add-azureanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 8793360953dbd705a41b3a3e746c94e55d659156
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679004"
---
# <span data-ttu-id="d64a6-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d64a6-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="d64a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d64a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d64a6-103">Az Azure Analysis Services kiszolgálói parancsmag-kérelmekhez használt hitelesített fiók hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d64a6-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d64a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d64a6-104">SYNTAX</span></span>

### <span data-ttu-id="d64a6-105">UserParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d64a6-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64a6-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d64a6-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64a6-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d64a6-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d64a6-108">DESCRIPTION</span></span>
<span data-ttu-id="d64a6-109">A Add-AzureAnalysisServicesAccount parancsmag az Azure Analysis Services-kiszolgáló egy példányához való bejelentkezéskor használatos.</span><span class="sxs-lookup"><span data-stu-id="d64a6-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="d64a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d64a6-110">EXAMPLES</span></span>

### <span data-ttu-id="d64a6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d64a6-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="d64a6-112">Ebben a példában a $UserCredential változó által megadott fiókot fogja hozzáadni a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="d64a6-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="d64a6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d64a6-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="d64a6-114">Az első parancs megkapja az Application Service Principal hitelesítő adatait, majd a $ApplicationCredential változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d64a6-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="d64a6-115">A második parancs hozzáadja a $ApplicationCredential változó és a bérlői azonosító megkeresése által megadott Application Service Principal-fiókot a westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="d64a6-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="d64a6-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="d64a6-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="d64a6-117">Ebben a példában a ApplicationId, az bérlői azonosító megkeresése és a CertificateThumbprint által megadott Application Service Principal-fiókot fogja hozzáadni az westcentralus.asazure.windows.net Analysis Services-környezethez.</span><span class="sxs-lookup"><span data-stu-id="d64a6-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="d64a6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d64a6-118">PARAMETERS</span></span>

### <span data-ttu-id="d64a6-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d64a6-119">-ApplicationId</span></span>
<span data-ttu-id="d64a6-120">Az alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d64a6-120">The application ID.</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d64a6-121">-CertificateThumbprint</span></span>
<span data-ttu-id="d64a6-122">Certificate hash (ujjlenyomat)</span><span class="sxs-lookup"><span data-stu-id="d64a6-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-123">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="d64a6-123">-Credential</span></span>
<span data-ttu-id="d64a6-124">Bejelentkezési hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="d64a6-124">Login credentials</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="d64a6-125">-RolloutEnvironment</span></span>
<span data-ttu-id="d64a6-126">Annak az Azure Analysis Services-környezetnek a neve, amelybe be szeretne jelentkezni.</span><span class="sxs-lookup"><span data-stu-id="d64a6-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="d64a6-127">A kiszolgáló teljes neve (például asazure://westcentralus.asazure.windows.net/testserver) esetén a változó helyes értéke lesz westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="d64a6-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: String
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d64a6-128">-ServicePrincipal</span></span>
<span data-ttu-id="d64a6-129">Jelzi, hogy ez a fiók a szolgáltatás elsődleges hitelesítő adataival van hitelesítve.</span><span class="sxs-lookup"><span data-stu-id="d64a6-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-130">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="d64a6-130">-TenantId</span></span>
<span data-ttu-id="d64a6-131">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="d64a6-131">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d64a6-132">-Confirm</span></span>
<span data-ttu-id="d64a6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d64a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64a6-134">-WhatIf</span></span>
<span data-ttu-id="d64a6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d64a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d64a6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d64a6-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d64a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64a6-137">CommonParameters</span></span>
<span data-ttu-id="d64a6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d64a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64a6-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64a6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64a6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d64a6-140">INPUTS</span></span>

### <span data-ttu-id="d64a6-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="d64a6-141">None</span></span>
<span data-ttu-id="d64a6-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d64a6-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d64a6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d64a6-143">OUTPUTS</span></span>

### <span data-ttu-id="d64a6-144">Microsoft. Azure. Command. AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d64a6-144">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="d64a6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d64a6-145">NOTES</span></span>
<span data-ttu-id="d64a6-146">Alias: Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="d64a6-146">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="d64a6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d64a6-147">RELATED LINKS</span></span>

