---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: c96fceb331a2b33528b47506e928ea78cfc793d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929850"
---
# <span data-ttu-id="129dc-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="129dc-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="129dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="129dc-102">SYNOPSIS</span></span>
<span data-ttu-id="129dc-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="129dc-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="129dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="129dc-104">SYNTAX</span></span>

### <span data-ttu-id="129dc-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="129dc-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129dc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="129dc-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129dc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="129dc-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129dc-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="129dc-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="129dc-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="129dc-109">DESCRIPTION</span></span>
<span data-ttu-id="129dc-110">A Get-AzADAppCredential parancsmag egy alkalmazáshoz társított hitelesítő adatok listájának beolvasásához használható.</span><span class="sxs-lookup"><span data-stu-id="129dc-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="129dc-111">Ez a parancs beolvassa az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de a hitelesítő adatok értékét nem).</span><span class="sxs-lookup"><span data-stu-id="129dc-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="129dc-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="129dc-112">EXAMPLES</span></span>

### <span data-ttu-id="129dc-113">1. példa: Alkalmazás hitelesítő adatainak lekérte objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="129dc-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="129dc-114">Visszaadja az "1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítóval rendelkező alkalmazás hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="129dc-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="129dc-115">2. példa: Alkalmazás hitelesítő adatainak be szereznie a pipázással</span><span class="sxs-lookup"><span data-stu-id="129dc-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="129dc-116">Az "1f99cf81-0146-4f4e-beae-2007d0668476" objektumazonosítót használja, és a Get-AzADAppCredential-parancsmagba becsatolta az alkalmazás összes hitelesítő adatát.</span><span class="sxs-lookup"><span data-stu-id="129dc-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="129dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="129dc-117">PARAMETERS</span></span>

### <span data-ttu-id="129dc-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="129dc-118">-ApplicationId</span></span>
<span data-ttu-id="129dc-119">Annak az alkalmazásnak az azonosítója, amelyből a hitelesítő adatokat beolvassa.</span><span class="sxs-lookup"><span data-stu-id="129dc-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="129dc-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="129dc-120">-ApplicationObject</span></span>
<span data-ttu-id="129dc-121">Az alkalmazásobjektum, amelyből a hitelesítő adatokat beolvassa.</span><span class="sxs-lookup"><span data-stu-id="129dc-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="129dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129dc-122">-DefaultProfile</span></span>
<span data-ttu-id="129dc-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="129dc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="129dc-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="129dc-124">-DisplayName</span></span>
<span data-ttu-id="129dc-125">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="129dc-125">The display name of the application.</span></span>

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

### <span data-ttu-id="129dc-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="129dc-126">-ObjectId</span></span>
<span data-ttu-id="129dc-127">Az alkalmazás objektumazonosítója, amelyből a hitelesítő adatokat lekéri.</span><span class="sxs-lookup"><span data-stu-id="129dc-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="129dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129dc-128">CommonParameters</span></span>
<span data-ttu-id="129dc-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="129dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129dc-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="129dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129dc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="129dc-131">INPUTS</span></span>

### <span data-ttu-id="129dc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="129dc-132">System.String</span></span>

### <span data-ttu-id="129dc-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="129dc-133">System.Guid</span></span>

### <span data-ttu-id="129dc-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="129dc-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="129dc-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="129dc-135">OUTPUTS</span></span>

### <span data-ttu-id="129dc-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="129dc-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="129dc-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="129dc-137">NOTES</span></span>

## <span data-ttu-id="129dc-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="129dc-138">RELATED LINKS</span></span>

[<span data-ttu-id="129dc-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="129dc-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="129dc-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="129dc-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="129dc-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="129dc-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

