---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016218"
---
# <span data-ttu-id="1be26-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1be26-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="1be26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1be26-102">SYNOPSIS</span></span>
<span data-ttu-id="1be26-103">Létrehozza a szükséges fájlokat és konfigurációt egy új szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1be26-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="1be26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1be26-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1be26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1be26-105">DESCRIPTION</span></span>
<span data-ttu-id="1be26-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="1be26-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1be26-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1be26-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1be26-108">A **New-AzureServiceProject** parancsmag létrehoz egy új Azure-szolgáltatás szükséges fájljait és konfigurációját az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="1be26-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="1be26-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1be26-109">EXAMPLES</span></span>

### <span data-ttu-id="1be26-110">1. példa: Állványzat létrehozása szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="1be26-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="1be26-111">Ez a példa állványzatot hoz létre egy MyService1 nevű új Azure-szolgáltatáshoz az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="1be26-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="1be26-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1be26-112">PARAMETERS</span></span>

### <span data-ttu-id="1be26-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="1be26-113">-Profile</span></span>
<span data-ttu-id="1be26-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1be26-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1be26-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1be26-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1be26-116">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="1be26-116">-ServiceName</span></span>
<span data-ttu-id="1be26-117">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1be26-117">Specifies the name of the service.</span></span>
<span data-ttu-id="1be26-118">Meghatározza a szolgáltatáshoz tartozó állomásnév első szakaszát (például name.cloudapp.net), valamint azt a címtárat, amely a szolgáltatást fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="1be26-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="1be26-119">A név csak betűket, számokat és kötőjel karaktert tartalmazhat (-).</span><span class="sxs-lookup"><span data-stu-id="1be26-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="1be26-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be26-120">CommonParameters</span></span>
<span data-ttu-id="1be26-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1be26-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be26-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be26-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be26-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1be26-123">INPUTS</span></span>

## <span data-ttu-id="1be26-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1be26-124">OUTPUTS</span></span>

## <span data-ttu-id="1be26-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1be26-125">NOTES</span></span>

## <span data-ttu-id="1be26-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1be26-126">RELATED LINKS</span></span>

[<span data-ttu-id="1be26-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="1be26-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="1be26-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="1be26-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="1be26-129">Közzététel – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1be26-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="1be26-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1be26-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="1be26-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="1be26-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


