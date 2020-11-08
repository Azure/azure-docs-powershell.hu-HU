---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015613"
---
# <span data-ttu-id="46052-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="46052-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="46052-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46052-102">SYNOPSIS</span></span>
<span data-ttu-id="46052-103">Megkapja a névteret.</span><span class="sxs-lookup"><span data-stu-id="46052-103">Gets the namespace.</span></span>


## <span data-ttu-id="46052-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46052-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46052-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46052-105">DESCRIPTION</span></span>
<span data-ttu-id="46052-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="46052-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="46052-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="46052-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="46052-108">A **Get-AzureSBNamespace** parancsmag az aktuális előfizetéshez társított Service Bus szolgáltatás névtereit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="46052-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="46052-109">Példák</span><span class="sxs-lookup"><span data-stu-id="46052-109">EXAMPLES</span></span>

### <span data-ttu-id="46052-110">1. példa: a szolgáltatási busz névterének beszerzése</span><span class="sxs-lookup"><span data-stu-id="46052-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="46052-111">Ez a példa beilleszti az aktuális előfizetéshez társított Service Bus szolgáltatás névtereit.</span><span class="sxs-lookup"><span data-stu-id="46052-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="46052-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46052-112">PARAMETERS</span></span>

### <span data-ttu-id="46052-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46052-113">-Name</span></span>
<span data-ttu-id="46052-114">Annak a szolgáltatásnak a nevét adja meg, amelyet meg szeretne keresni.</span><span class="sxs-lookup"><span data-stu-id="46052-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="46052-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="46052-115">-Profile</span></span>
<span data-ttu-id="46052-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="46052-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46052-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="46052-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46052-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46052-118">CommonParameters</span></span>
<span data-ttu-id="46052-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46052-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46052-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46052-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46052-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46052-121">INPUTS</span></span>

## <span data-ttu-id="46052-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46052-122">OUTPUTS</span></span>

## <span data-ttu-id="46052-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46052-123">NOTES</span></span>

## <span data-ttu-id="46052-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46052-124">RELATED LINKS</span></span>

[<span data-ttu-id="46052-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="46052-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


