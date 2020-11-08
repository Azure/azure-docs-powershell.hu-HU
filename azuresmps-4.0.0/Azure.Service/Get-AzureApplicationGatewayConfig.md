---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015665"
---
# <span data-ttu-id="09b72-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="09b72-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="09b72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09b72-102">SYNOPSIS</span></span>
<span data-ttu-id="09b72-103">Az alkalmazás-átjáró konfigurációs környezetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="09b72-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="09b72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09b72-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="09b72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09b72-105">DESCRIPTION</span></span>
<span data-ttu-id="09b72-106">A **Get-AzureApplicationGatewayConfig** parancsmag Azure Application Gateway-konfigurációs környezetet kap.</span><span class="sxs-lookup"><span data-stu-id="09b72-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="09b72-107">A kontextusban konfigurációs objektum és XML-konfiguráció is szerepel.</span><span class="sxs-lookup"><span data-stu-id="09b72-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="09b72-108">Az XML-konfigurációt mentheti fájlba.</span><span class="sxs-lookup"><span data-stu-id="09b72-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="09b72-109">Példák</span><span class="sxs-lookup"><span data-stu-id="09b72-109">EXAMPLES</span></span>

### <span data-ttu-id="09b72-110">1. példa: alkalmazás-átjáró beállítása és mentése fájlba</span><span class="sxs-lookup"><span data-stu-id="09b72-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="09b72-111">Ez a parancs a ApplicationGateway06 nevű alkalmazás-átjáró konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="09b72-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="09b72-112">A parancs a megadott elérési útnak megfelelő fájlba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="09b72-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="09b72-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09b72-113">PARAMETERS</span></span>

### <span data-ttu-id="09b72-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="09b72-114">-ExportToFile</span></span>
<span data-ttu-id="09b72-115">Annak a fájlnak az elérési útját adja meg, amelyre a parancsmag XML formátumban menti a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="09b72-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b72-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09b72-116">-Name</span></span>
<span data-ttu-id="09b72-117">Annak az alkalmazás-átjárónak a neve, amelyhez ez a parancsmag konfigurációs információkat kap.</span><span class="sxs-lookup"><span data-stu-id="09b72-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09b72-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="09b72-118">-Profile</span></span>
<span data-ttu-id="09b72-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="09b72-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="09b72-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="09b72-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b72-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b72-121">CommonParameters</span></span>
<span data-ttu-id="09b72-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09b72-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b72-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b72-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b72-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09b72-124">INPUTS</span></span>

### <span data-ttu-id="09b72-125">System. String</span><span class="sxs-lookup"><span data-stu-id="09b72-125">System.String</span></span>

## <span data-ttu-id="09b72-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09b72-126">OUTPUTS</span></span>

### <span data-ttu-id="09b72-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="09b72-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="09b72-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09b72-128">NOTES</span></span>

## <span data-ttu-id="09b72-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09b72-129">RELATED LINKS</span></span>

[<span data-ttu-id="09b72-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="09b72-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


