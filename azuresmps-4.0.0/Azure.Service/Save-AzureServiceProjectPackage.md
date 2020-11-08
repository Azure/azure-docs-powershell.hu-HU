---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015460"
---
# <span data-ttu-id="a776c-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="a776c-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="a776c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a776c-102">SYNOPSIS</span></span>
<span data-ttu-id="a776c-103">Becsomagolja a szolgáltatás projektjét az Azure Cloud csomagba.</span><span class="sxs-lookup"><span data-stu-id="a776c-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="a776c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a776c-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a776c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a776c-105">DESCRIPTION</span></span>
<span data-ttu-id="a776c-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a776c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a776c-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a776c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a776c-108">A **Save-AzureServiceProjectPackage** parancsmag a szolgáltatás projektjét Azure Cloud Package (\*. cspkg) csomagba csomagolja.</span><span class="sxs-lookup"><span data-stu-id="a776c-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="a776c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a776c-109">EXAMPLES</span></span>

### <span data-ttu-id="a776c-110">1. példa: projekt-csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="a776c-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="a776c-111">Ez a példa létrehoz egy \*. cspgk a MyAzureServiceProject nevű szolgáltatási projekthez.</span><span class="sxs-lookup"><span data-stu-id="a776c-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="a776c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a776c-112">PARAMETERS</span></span>

### <span data-ttu-id="a776c-113">-Local (helyi)</span><span class="sxs-lookup"><span data-stu-id="a776c-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a776c-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="a776c-114">-Profile</span></span>
<span data-ttu-id="a776c-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a776c-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a776c-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a776c-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a776c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a776c-117">CommonParameters</span></span>
<span data-ttu-id="a776c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a776c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a776c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a776c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a776c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a776c-120">INPUTS</span></span>

## <span data-ttu-id="a776c-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a776c-121">OUTPUTS</span></span>

## <span data-ttu-id="a776c-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a776c-122">NOTES</span></span>

## <span data-ttu-id="a776c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a776c-123">RELATED LINKS</span></span>

[<span data-ttu-id="a776c-124">Közzététel – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a776c-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


