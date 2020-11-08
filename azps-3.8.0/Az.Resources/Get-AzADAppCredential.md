---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: ef03850e2a8c0981ad4a1b642df51c1fec462513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012029"
---
# <span data-ttu-id="d2524-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d2524-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="d2524-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2524-102">SYNOPSIS</span></span>
<span data-ttu-id="d2524-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="d2524-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="d2524-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2524-104">SYNTAX</span></span>

### <span data-ttu-id="d2524-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2524-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2524-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2524-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2524-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2524-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2524-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2524-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2524-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2524-109">DESCRIPTION</span></span>
<span data-ttu-id="d2524-110">Az Get-AzADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="d2524-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="d2524-111">Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.</span><span class="sxs-lookup"><span data-stu-id="d2524-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="d2524-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d2524-112">EXAMPLES</span></span>

### <span data-ttu-id="d2524-113">Példa 1 – alkalmazásspecifikus hitelesítő adatok beszerzése objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="d2524-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="d2524-114">A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d2524-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="d2524-115">2 példa – az alkalmazás hitelesítő adatainak beolvasása csővezetéken</span><span class="sxs-lookup"><span data-stu-id="d2524-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="d2524-116">Beilleszti az alkalmazást a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektumazonosítót, és a Get-AzADAppCredential parancsmaghoz illeszti az adott alkalmazás összes hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="d2524-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="d2524-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2524-117">PARAMETERS</span></span>

### <span data-ttu-id="d2524-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d2524-118">-ApplicationId</span></span>
<span data-ttu-id="d2524-119">Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="d2524-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d2524-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d2524-120">-ApplicationObject</span></span>
<span data-ttu-id="d2524-121">Az Application objektum a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="d2524-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d2524-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2524-122">-DefaultProfile</span></span>
<span data-ttu-id="d2524-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d2524-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2524-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d2524-124">-DisplayName</span></span>
<span data-ttu-id="d2524-125">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="d2524-125">The display name of the application.</span></span>

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

### <span data-ttu-id="d2524-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d2524-126">-ObjectId</span></span>
<span data-ttu-id="d2524-127">A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d2524-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d2524-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2524-128">CommonParameters</span></span>
<span data-ttu-id="d2524-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2524-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2524-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2524-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2524-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2524-131">INPUTS</span></span>

### <span data-ttu-id="d2524-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d2524-132">System.String</span></span>

### <span data-ttu-id="d2524-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d2524-133">System.Guid</span></span>

### <span data-ttu-id="d2524-134">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d2524-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d2524-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2524-135">OUTPUTS</span></span>

### <span data-ttu-id="d2524-136">Microsoft. Azure. Command. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="d2524-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="d2524-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2524-137">NOTES</span></span>

## <span data-ttu-id="d2524-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2524-138">RELATED LINKS</span></span>

[<span data-ttu-id="d2524-139">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d2524-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="d2524-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d2524-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="d2524-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d2524-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

