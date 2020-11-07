---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fc8e454328706243e701c0f4df61733562ab73ce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843482"
---
# <span data-ttu-id="e0875-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e0875-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="e0875-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0875-102">SYNOPSIS</span></span>
<span data-ttu-id="e0875-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="e0875-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="e0875-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0875-104">SYNTAX</span></span>

### <span data-ttu-id="e0875-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0875-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0875-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0875-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0875-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0875-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0875-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0875-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0875-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0875-109">DESCRIPTION</span></span>
<span data-ttu-id="e0875-110">Az Get-AzADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="e0875-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="e0875-111">Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.</span><span class="sxs-lookup"><span data-stu-id="e0875-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="e0875-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e0875-112">EXAMPLES</span></span>

### <span data-ttu-id="e0875-113">Példa 1 – alkalmazásspecifikus hitelesítő adatok beszerzése objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="e0875-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="e0875-114">A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e0875-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="e0875-115">2 példa – az alkalmazás hitelesítő adatainak beolvasása csővezetéken</span><span class="sxs-lookup"><span data-stu-id="e0875-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="e0875-116">Beilleszti az alkalmazást a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektumazonosítót, és a Get-AzADAppCredential parancsmaghoz illeszti az adott alkalmazás összes hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="e0875-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="e0875-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0875-117">PARAMETERS</span></span>

### <span data-ttu-id="e0875-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e0875-118">-ApplicationId</span></span>
<span data-ttu-id="e0875-119">Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="e0875-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e0875-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e0875-120">-ApplicationObject</span></span>
<span data-ttu-id="e0875-121">Az Application objektum a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="e0875-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0875-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0875-122">-DefaultProfile</span></span>
<span data-ttu-id="e0875-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0875-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0875-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e0875-124">-DisplayName</span></span>
<span data-ttu-id="e0875-125">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="e0875-125">The display name of the application.</span></span>

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

### <span data-ttu-id="e0875-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e0875-126">-ObjectId</span></span>
<span data-ttu-id="e0875-127">A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0875-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0875-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0875-128">CommonParameters</span></span>
<span data-ttu-id="e0875-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0875-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0875-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0875-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0875-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0875-131">INPUTS</span></span>

### <span data-ttu-id="e0875-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e0875-132">System.Guid</span></span>

### <span data-ttu-id="e0875-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e0875-133">System.String</span></span>

### <span data-ttu-id="e0875-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e0875-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="e0875-135">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e0875-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="e0875-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0875-136">OUTPUTS</span></span>

### <span data-ttu-id="e0875-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e0875-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e0875-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0875-138">NOTES</span></span>

## <span data-ttu-id="e0875-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0875-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0875-140">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e0875-140">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e0875-141">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e0875-141">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e0875-142">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e0875-142">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

