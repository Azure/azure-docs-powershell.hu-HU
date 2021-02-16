---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149682"
---
# <span data-ttu-id="d43e5-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d43e5-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="d43e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d43e5-103">Létrehoz egy appszolgáltatás által felügyelt tanúsítványt egy Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="d43e5-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="d43e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d43e5-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d43e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d43e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d43e5-106">A **New-AzWebAppCertificate** parancsmag létrehoz egy Azure App Service Felügyelt tanúsítványt</span><span class="sxs-lookup"><span data-stu-id="d43e5-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="d43e5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d43e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d43e5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d43e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="d43e5-109">Ez a parancs appszolgáltatás által felügyelt tanúsítványt hoz létre az adott WebApphoz</span><span class="sxs-lookup"><span data-stu-id="d43e5-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="d43e5-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d43e5-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="d43e5-111">Ez a parancs létrehoz egy appszolgáltatás által felügyelt tanúsítványt, és a megadott webapphelyhez kötődik.</span><span class="sxs-lookup"><span data-stu-id="d43e5-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="d43e5-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="d43e5-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="d43e5-113">Ez a parancs létrehoz egy appszolgáltatás által felügyelt tanúsítványt, és a megadott WebApphoz kötődik.</span><span class="sxs-lookup"><span data-stu-id="d43e5-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="d43e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d43e5-114">PARAMETERS</span></span>

### <span data-ttu-id="d43e5-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="d43e5-115">-AddBinding</span></span>
<span data-ttu-id="d43e5-116">A létrehozott tanúsítvány hozzáadása a WebApp/slot alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="d43e5-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43e5-117">-DefaultProfile</span></span>
<span data-ttu-id="d43e5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d43e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="d43e5-119">-HostName</span></span>
<span data-ttu-id="d43e5-120">A webalkalmazáshoz/-tárolóhelyhez társított egyéni állomásnevek.</span><span class="sxs-lookup"><span data-stu-id="d43e5-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d43e5-121">-Name</span></span>
<span data-ttu-id="d43e5-122">A tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="d43e5-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d43e5-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d43e5-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="d43e5-125">-Slot</span></span>
<span data-ttu-id="d43e5-126">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="d43e5-126">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="d43e5-127">-SslState</span></span>
<span data-ttu-id="d43e5-128">Ssl-állapot beállítás.</span><span class="sxs-lookup"><span data-stu-id="d43e5-128">Ssl state option.</span></span>
<span data-ttu-id="d43e5-129">Használja a "SniEnabled" vagy az "IpBasedEnabled" címet.</span><span class="sxs-lookup"><span data-stu-id="d43e5-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="d43e5-130">Az alapértelmezett beállítás a "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="d43e5-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="d43e5-131">-WebAppName</span></span>
<span data-ttu-id="d43e5-132">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="d43e5-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43e5-133">CommonParameters</span></span>
<span data-ttu-id="d43e5-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43e5-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d43e5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43e5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d43e5-136">INPUTS</span></span>

### <span data-ttu-id="d43e5-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="d43e5-137">None</span></span>

## <span data-ttu-id="d43e5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d43e5-138">OUTPUTS</span></span>

### <span data-ttu-id="d43e5-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="d43e5-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="d43e5-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d43e5-140">NOTES</span></span>

## <span data-ttu-id="d43e5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d43e5-141">RELATED LINKS</span></span>
[<span data-ttu-id="d43e5-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="d43e5-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)