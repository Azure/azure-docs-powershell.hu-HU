---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015988"
---
# <span data-ttu-id="520eb-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="520eb-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="520eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="520eb-102">SYNOPSIS</span></span>
<span data-ttu-id="520eb-103">Névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="520eb-103">Creates a namespace.</span></span>

## <span data-ttu-id="520eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="520eb-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="520eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="520eb-105">DESCRIPTION</span></span>
<span data-ttu-id="520eb-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="520eb-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="520eb-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="520eb-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="520eb-108">A **New-AzureSBNamespace** parancsmag létrehoz egy szolgáltatási névteret, amellyel az Azure rendszerhez használható a szolgáltatás busza.</span><span class="sxs-lookup"><span data-stu-id="520eb-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="520eb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="520eb-109">EXAMPLES</span></span>

### <span data-ttu-id="520eb-110">Példa 1: szolgáltatásbeli névtér létrehozása</span><span class="sxs-lookup"><span data-stu-id="520eb-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="520eb-111">A példákban létrehoz egy szolgáltatási névteret, amellyel az Azure-ban használható a szolgáltatás busza.</span><span class="sxs-lookup"><span data-stu-id="520eb-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="520eb-112">Mindkét példa tartalmazza a szükséges paramétereket, a paramétereket azonban csak az első tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="520eb-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="520eb-113">A második példa akkor használható, ha mindkét paraméter pozícióval van megadva, és az értékek a szükséges sorrendben jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="520eb-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="520eb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="520eb-114">PARAMETERS</span></span>

### <span data-ttu-id="520eb-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="520eb-115">-CreateACSNamespace</span></span>
<span data-ttu-id="520eb-116">Azt adja meg, hogy a szolgáltatás névterén kívül létre kell-e hozni egy kapcsolódó ACS-névteret.</span><span class="sxs-lookup"><span data-stu-id="520eb-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520eb-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="520eb-117">-Location</span></span>
<span data-ttu-id="520eb-118">Az új névtér területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="520eb-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="520eb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="520eb-119">-Name</span></span>
<span data-ttu-id="520eb-120">Az új névtér nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="520eb-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="520eb-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="520eb-121">-NamespaceType</span></span>
<span data-ttu-id="520eb-122">Adja meg, hogy a névteret szeretné-e használni az üzenetküldési vagy az értesítési hubok számára.</span><span class="sxs-lookup"><span data-stu-id="520eb-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520eb-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="520eb-123">-Profile</span></span>
<span data-ttu-id="520eb-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="520eb-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="520eb-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="520eb-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="520eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520eb-126">CommonParameters</span></span>
<span data-ttu-id="520eb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="520eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520eb-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="520eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520eb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="520eb-129">INPUTS</span></span>

## <span data-ttu-id="520eb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="520eb-130">OUTPUTS</span></span>

## <span data-ttu-id="520eb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="520eb-131">NOTES</span></span>

## <span data-ttu-id="520eb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="520eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="520eb-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="520eb-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


