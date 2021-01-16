---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333173"
---
# <span data-ttu-id="5b778-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="5b778-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="5b778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b778-102">SYNOPSIS</span></span>
<span data-ttu-id="5b778-103">Nyers hozzáférési jogkivonat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="5b778-103">Get raw access token.</span></span> <span data-ttu-id="5b778-104">A -ResourceUrl használata esetén ellenőrizze, hogy az érték megfelel-e az aktuális Azure-környezetnek.</span><span class="sxs-lookup"><span data-stu-id="5b778-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="5b778-105">Hivatkozhat a `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="5b778-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="5b778-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b778-106">SYNTAX</span></span>

### <span data-ttu-id="5b778-107">KnownResourceTypeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b778-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b778-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="5b778-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b778-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b778-109">DESCRIPTION</span></span>
<span data-ttu-id="5b778-110">Hozzáférési jogkivonat beszerzése</span><span class="sxs-lookup"><span data-stu-id="5b778-110">Get access token</span></span>

## <span data-ttu-id="5b778-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b778-111">EXAMPLES</span></span>

### <span data-ttu-id="5b778-112">1. példa: Nyers hozzáférési jogkivonat beszerzése ARM végponthoz</span><span class="sxs-lookup"><span data-stu-id="5b778-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="5b778-113">Az aktuális fiók ResourceManager-végpontjának hozzáférési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5b778-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="5b778-114">2. példa: Nyers hozzáférési jogkivonat beszerzése az AAD Graph-végponthoz</span><span class="sxs-lookup"><span data-stu-id="5b778-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="5b778-115">Az aktuális fiók AAD Graph-végpontjának hozzáférési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5b778-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="5b778-116">3. példa: Nyers hozzáférési jogkivonat beszerzése az AAD Graph-végponthoz</span><span class="sxs-lookup"><span data-stu-id="5b778-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="5b778-117">Az aktuális fiók AAD Graph-végpontjának hozzáférési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5b778-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="5b778-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b778-118">PARAMETERS</span></span>

### <span data-ttu-id="5b778-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b778-119">-DefaultProfile</span></span>
<span data-ttu-id="5b778-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b778-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b778-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="5b778-121">-ResourceTypeName</span></span>
<span data-ttu-id="5b778-122">Nem kötelező megadni a típus nevét, támogatott értékek: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="5b778-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="5b778-123">Az alapértelmezett érték az Arm, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="5b778-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b778-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="5b778-124">-ResourceUrl</span></span>
<span data-ttu-id="5b778-125">Annak az erőforrásnak az URL-címe, amelyhez jogkivonatot kér, például ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="5b778-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b778-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5b778-126">-TenantId</span></span>
<span data-ttu-id="5b778-127">Nem kötelező bérlőazonosító. Ha nincs megadva, használja az alapértelmezett környezet bérlőazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="5b778-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="5b778-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b778-128">CommonParameters</span></span>
<span data-ttu-id="5b778-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b778-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b778-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b778-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b778-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b778-131">INPUTS</span></span>

### <span data-ttu-id="5b778-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b778-132">None</span></span>

## <span data-ttu-id="5b778-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b778-133">OUTPUTS</span></span>

### <span data-ttu-id="5b778-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5b778-134">System.String</span></span>

## <span data-ttu-id="5b778-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b778-135">NOTES</span></span>

## <span data-ttu-id="5b778-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b778-136">RELATED LINKS</span></span>
