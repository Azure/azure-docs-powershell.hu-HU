---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015670"
---
# <span data-ttu-id="7821c-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="7821c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7821c-102">SYNOPSIS</span></span>
<span data-ttu-id="7821c-103">Bekerül egy alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="7821c-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="7821c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7821c-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7821c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7821c-105">DESCRIPTION</span></span>
<span data-ttu-id="7821c-106">A **Get-AzureApplicationGateway** parancsmag meglévő Azure Application Gatewayt kap.</span><span class="sxs-lookup"><span data-stu-id="7821c-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="7821c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7821c-107">EXAMPLES</span></span>

### <span data-ttu-id="7821c-108">1. példa: alkalmazás-átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="7821c-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="7821c-109">Ez a parancs a ApplicationGateway06 nevű alkalmazás-átjárót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7821c-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="7821c-110">2. példa: az összes alkalmazás-átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="7821c-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="7821c-111">Ez a parancs beilleszti az összes alkalmazás-átjárót az előfizetése alatt.</span><span class="sxs-lookup"><span data-stu-id="7821c-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="7821c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7821c-112">PARAMETERS</span></span>

### <span data-ttu-id="7821c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7821c-113">-Name</span></span>
<span data-ttu-id="7821c-114">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7821c-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7821c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7821c-115">-Profile</span></span>
<span data-ttu-id="7821c-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7821c-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7821c-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7821c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7821c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7821c-118">CommonParameters</span></span>
<span data-ttu-id="7821c-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7821c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7821c-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7821c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7821c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7821c-121">INPUTS</span></span>

### <span data-ttu-id="7821c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="7821c-122">System.String</span></span>

## <span data-ttu-id="7821c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7821c-123">OUTPUTS</span></span>

### <span data-ttu-id="7821c-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="7821c-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="7821c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7821c-125">NOTES</span></span>

## <span data-ttu-id="7821c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7821c-126">RELATED LINKS</span></span>

[<span data-ttu-id="7821c-127">Új – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="7821c-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="7821c-129">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="7821c-130">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="7821c-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7821c-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


