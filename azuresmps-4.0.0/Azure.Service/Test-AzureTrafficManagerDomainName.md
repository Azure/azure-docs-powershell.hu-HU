---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015935"
---
# <span data-ttu-id="bce37-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="bce37-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="bce37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bce37-102">SYNOPSIS</span></span>
<span data-ttu-id="bce37-103">Ellenőrzi, hogy egy tartománynév elérhető-e Traffic Manager-profilként.</span><span class="sxs-lookup"><span data-stu-id="bce37-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="bce37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bce37-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bce37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bce37-105">DESCRIPTION</span></span>
<span data-ttu-id="bce37-106">A **AzureTrafficManagerDomainName-** parancsmag ellenőrzi, hogy egy tartománynév elérhető-e Microsoft Azure Traffic Manager-profilként.</span><span class="sxs-lookup"><span data-stu-id="bce37-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bce37-107">Ha a tartománynév elérhető, a parancsmag a $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bce37-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="bce37-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bce37-108">EXAMPLES</span></span>

### <span data-ttu-id="bce37-109">Példa 1: annak ellenőrzése, hogy elérhető-e tartománynév</span><span class="sxs-lookup"><span data-stu-id="bce37-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="bce37-110">Ez a parancs azt ellenőrzi, hogy a tartománynév ContosoApp.trafficmanager.net elérhető-e Traffic Manager-profilként.</span><span class="sxs-lookup"><span data-stu-id="bce37-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="bce37-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bce37-111">PARAMETERS</span></span>

### <span data-ttu-id="bce37-112">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="bce37-112">-DomainName</span></span>
<span data-ttu-id="bce37-113">A tesztelni kívánt tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bce37-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="bce37-114">A következő karakterláncot kell tartalmaznia:</span><span class="sxs-lookup"><span data-stu-id="bce37-114">You must include the following string:</span></span> 

<span data-ttu-id="bce37-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="bce37-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce37-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="bce37-116">-Profile</span></span>
<span data-ttu-id="bce37-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="bce37-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bce37-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="bce37-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bce37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce37-119">CommonParameters</span></span>
<span data-ttu-id="bce37-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bce37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce37-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce37-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce37-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce37-122">INPUTS</span></span>

## <span data-ttu-id="bce37-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce37-123">OUTPUTS</span></span>

### <span data-ttu-id="bce37-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce37-124">System.Boolean</span></span>
<span data-ttu-id="bce37-125">Ez a parancsmag $True vagy $Falset hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bce37-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="bce37-126">Ha a tartománynév elérhető, a parancsmag a $True értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bce37-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="bce37-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bce37-127">NOTES</span></span>

## <span data-ttu-id="bce37-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce37-128">RELATED LINKS</span></span>

