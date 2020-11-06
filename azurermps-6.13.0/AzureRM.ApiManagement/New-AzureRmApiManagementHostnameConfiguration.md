---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: defd5c046427115e44783d6b34ea7b034edc8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492920"
---
# <span data-ttu-id="57d61-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="57d61-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="57d61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57d61-102">SYNOPSIS</span></span>
<span data-ttu-id="57d61-103">Létrehozza a PsApiManagementHostnameConfiguration példányát.</span><span class="sxs-lookup"><span data-stu-id="57d61-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57d61-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57d61-105">DESCRIPTION</span></span>
<span data-ttu-id="57d61-106">A **New-AzureRmApiManagementHostnameConfiguration** parancsmag egy olyan segítő parancs, amely a **PsApiManagementHostnameConfiguration** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="57d61-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="57d61-107">Ezt a parancsot a Set-AzureRmApiManagementHostnames parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="57d61-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="57d61-108">Példák</span><span class="sxs-lookup"><span data-stu-id="57d61-108">EXAMPLES</span></span>

### <span data-ttu-id="57d61-109">1. példa: PsApiManagementHostnameConfiguration-példány létrehozása és inicializálása</span><span class="sxs-lookup"><span data-stu-id="57d61-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="57d61-110">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementHostnameConfiguration** példányát.</span><span class="sxs-lookup"><span data-stu-id="57d61-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="57d61-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57d61-111">PARAMETERS</span></span>

### <span data-ttu-id="57d61-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="57d61-112">-CertificateThumbprint</span></span>
<span data-ttu-id="57d61-113">A tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="57d61-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="57d61-114">A tanúsítványt először az Import-AzureRmApiManagementHostnameCertificate parancsmaggal kell importálni.</span><span class="sxs-lookup"><span data-stu-id="57d61-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d61-115">-DefaultProfile</span></span>
<span data-ttu-id="57d61-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57d61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d61-117">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="57d61-117">-Hostname</span></span>
<span data-ttu-id="57d61-118">Azt az egyéni állomásnevet adja meg, amelyhez a parancsmag létrehozta a **PsApiManagementHostnameConfiguration** -példányt.</span><span class="sxs-lookup"><span data-stu-id="57d61-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d61-119">CommonParameters</span></span>
<span data-ttu-id="57d61-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57d61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d61-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d61-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d61-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57d61-122">INPUTS</span></span>

### <span data-ttu-id="57d61-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="57d61-123">None</span></span>

## <span data-ttu-id="57d61-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57d61-124">OUTPUTS</span></span>

### <span data-ttu-id="57d61-125">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="57d61-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="57d61-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57d61-126">NOTES</span></span>

## <span data-ttu-id="57d61-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57d61-127">RELATED LINKS</span></span>

[<span data-ttu-id="57d61-128">Importálás – AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="57d61-128">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="57d61-129">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="57d61-129">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


