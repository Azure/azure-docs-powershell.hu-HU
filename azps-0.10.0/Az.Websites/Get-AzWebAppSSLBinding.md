---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842773"
---
# <span data-ttu-id="8bdac-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8bdac-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="8bdac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bdac-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdac-103">Az Azure Web App tanúsítványának SSL-kötését kapja.</span><span class="sxs-lookup"><span data-stu-id="8bdac-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="8bdac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bdac-104">SYNTAX</span></span>

### <span data-ttu-id="8bdac-105">S1</span><span class="sxs-lookup"><span data-stu-id="8bdac-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bdac-106">S2</span><span class="sxs-lookup"><span data-stu-id="8bdac-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bdac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bdac-107">DESCRIPTION</span></span>
<span data-ttu-id="8bdac-108">A **Get-AzWebAppSSLBinding** parancsmag Secure Sockets Layer (SSL) kötést kap az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8bdac-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="8bdac-109">Az SSL-kötések a webalkalmazások feltöltött tanúsítványsal való társítására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="8bdac-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="8bdac-110">A webes alkalmazások több tanúsítványhoz is kötve lehetnek.</span><span class="sxs-lookup"><span data-stu-id="8bdac-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="8bdac-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8bdac-111">EXAMPLES</span></span>

### <span data-ttu-id="8bdac-112">Példa 1: SSL-kötések beszerzése egy webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="8bdac-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="8bdac-113">Ez a parancs beolvassa a Web App ContosoWebApp az erőforráscsoport ContosoResourceGroup társított SSL-kötéseit.</span><span class="sxs-lookup"><span data-stu-id="8bdac-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="8bdac-114">2. példa: az SSL-kötések beszerzése egy webalkalmazáshoz objektum-hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="8bdac-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="8bdac-115">Az ebben a példában szereplő parancsok a Web App ContosoWebApp tartozó SSL-kötéseket is megkapják; Ebben az esetben azonban a Web App neve és a hozzá tartozó erőforráscsoport neve helyett egy objektum-hivatkozás van használatban.</span><span class="sxs-lookup"><span data-stu-id="8bdac-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="8bdac-116">Ezt az objektumot a példa első parancsa hozza létre, amely a **Get-AzWebApp** használatával hozza létre az objektum hivatkozását a ContosoWebApp nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="8bdac-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="8bdac-117">Az objektum hivatkozása $WebApp nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="8bdac-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="8bdac-118">Ezt a változót és a **Get-AzWebAppSSLBinding** parancsmagot a második parancs használja az SSL-kötések beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="8bdac-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="8bdac-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bdac-119">PARAMETERS</span></span>

### <span data-ttu-id="8bdac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdac-120">-DefaultProfile</span></span>
<span data-ttu-id="8bdac-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bdac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdac-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8bdac-122">-Name</span></span>
<span data-ttu-id="8bdac-123">Az SSL-kötés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8bdac-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="8bdac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdac-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bdac-125">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8bdac-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="8bdac-126">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="8bdac-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdac-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="8bdac-127">-Slot</span></span>
<span data-ttu-id="8bdac-128">Egy webalkalmazás-telepítő bővítőhelyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="8bdac-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="8bdac-129">Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8bdac-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdac-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8bdac-130">-WebApp</span></span>
<span data-ttu-id="8bdac-131">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="8bdac-131">Specifies a Web App.</span></span>
<span data-ttu-id="8bdac-132">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8bdac-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdac-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="8bdac-133">-WebAppName</span></span>
<span data-ttu-id="8bdac-134">Annak a webalkalmazásnak a nevét adja meg, amelynek a parancsmagja SSL-kötést kap.</span><span class="sxs-lookup"><span data-stu-id="8bdac-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="8bdac-135">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="8bdac-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdac-136">CommonParameters</span></span>
<span data-ttu-id="8bdac-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bdac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdac-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdac-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdac-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bdac-139">INPUTS</span></span>

### <span data-ttu-id="8bdac-140">Webhely</span><span class="sxs-lookup"><span data-stu-id="8bdac-140">Site</span></span>
<span data-ttu-id="8bdac-141">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8bdac-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8bdac-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bdac-142">OUTPUTS</span></span>

## <span data-ttu-id="8bdac-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bdac-143">NOTES</span></span>

## <span data-ttu-id="8bdac-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bdac-144">RELATED LINKS</span></span>

[<span data-ttu-id="8bdac-145">Új – AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8bdac-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="8bdac-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8bdac-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="8bdac-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8bdac-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


