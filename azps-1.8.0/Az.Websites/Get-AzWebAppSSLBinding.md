---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: a50716315796d46185b67099784bc550295231e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668350"
---
# <span data-ttu-id="2803c-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2803c-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="2803c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2803c-102">SYNOPSIS</span></span>
<span data-ttu-id="2803c-103">Az Azure Web App tanúsítványának SSL-kötését kapja.</span><span class="sxs-lookup"><span data-stu-id="2803c-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="2803c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2803c-104">SYNTAX</span></span>

### <span data-ttu-id="2803c-105">S1</span><span class="sxs-lookup"><span data-stu-id="2803c-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2803c-106">S2</span><span class="sxs-lookup"><span data-stu-id="2803c-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2803c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2803c-107">DESCRIPTION</span></span>
<span data-ttu-id="2803c-108">A **Get-AzWebAppSSLBinding** parancsmag Secure Sockets Layer (SSL) kötést kap az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="2803c-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="2803c-109">Az SSL-kötések a webalkalmazások feltöltött tanúsítványsal való társítására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="2803c-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="2803c-110">A webes alkalmazások több tanúsítványhoz is kötve lehetnek.</span><span class="sxs-lookup"><span data-stu-id="2803c-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="2803c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2803c-111">EXAMPLES</span></span>

### <span data-ttu-id="2803c-112">Példa 1: SSL-kötések beszerzése egy webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="2803c-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="2803c-113">Ez a parancs beolvassa a Web App ContosoWebApp az erőforráscsoport ContosoResourceGroup társított SSL-kötéseit.</span><span class="sxs-lookup"><span data-stu-id="2803c-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="2803c-114">2. példa: az SSL-kötések beszerzése egy webalkalmazáshoz objektum-hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="2803c-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="2803c-115">Az ebben a példában szereplő parancsok a Web App ContosoWebApp tartozó SSL-kötéseket is megkapják; Ebben az esetben azonban a Web App neve és a hozzá tartozó erőforráscsoport neve helyett egy objektum-hivatkozás van használatban.</span><span class="sxs-lookup"><span data-stu-id="2803c-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="2803c-116">Ezt az objektumot a példa első parancsa hozza létre, amely a **Get-AzWebApp** használatával hozza létre az objektum hivatkozását a ContosoWebApp nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="2803c-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="2803c-117">Az objektum hivatkozása $WebApp nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="2803c-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="2803c-118">Ezt a változót és a **Get-AzWebAppSSLBinding** parancsmagot a második parancs használja az SSL-kötések beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="2803c-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="2803c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2803c-119">PARAMETERS</span></span>

### <span data-ttu-id="2803c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2803c-120">-DefaultProfile</span></span>
<span data-ttu-id="2803c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2803c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2803c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2803c-122">-Name</span></span>
<span data-ttu-id="2803c-123">Az SSL-kötés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2803c-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2803c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2803c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2803c-125">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2803c-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="2803c-126">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="2803c-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2803c-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="2803c-127">-Slot</span></span>
<span data-ttu-id="2803c-128">Egy webalkalmazás-telepítő bővítőhelyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="2803c-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="2803c-129">Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2803c-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2803c-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2803c-130">-WebApp</span></span>
<span data-ttu-id="2803c-131">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="2803c-131">Specifies a Web App.</span></span>
<span data-ttu-id="2803c-132">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2803c-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2803c-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2803c-133">-WebAppName</span></span>
<span data-ttu-id="2803c-134">Annak a webalkalmazásnak a nevét adja meg, amelynek a parancsmagja SSL-kötést kap.</span><span class="sxs-lookup"><span data-stu-id="2803c-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="2803c-135">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="2803c-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2803c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2803c-136">CommonParameters</span></span>
<span data-ttu-id="2803c-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2803c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2803c-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2803c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2803c-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2803c-139">INPUTS</span></span>

### <span data-ttu-id="2803c-140">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2803c-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2803c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2803c-141">OUTPUTS</span></span>

### <span data-ttu-id="2803c-142">Microsoft. Azure. Management. WebSites. models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="2803c-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="2803c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2803c-143">NOTES</span></span>

## <span data-ttu-id="2803c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2803c-144">RELATED LINKS</span></span>

[<span data-ttu-id="2803c-145">Új – AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2803c-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="2803c-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2803c-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="2803c-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2803c-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


