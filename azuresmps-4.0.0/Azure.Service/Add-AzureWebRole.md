---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015711"
---
# <span data-ttu-id="d24d5-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="d24d5-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="d24d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d24d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d24d5-103">Webes munkatársi szerepkör felvétele</span><span class="sxs-lookup"><span data-stu-id="d24d5-103">Adds a web worker role.</span></span>

## <span data-ttu-id="d24d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d24d5-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d24d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d24d5-105">DESCRIPTION</span></span>
<span data-ttu-id="d24d5-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d24d5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d24d5-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d24d5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d24d5-108">Az **Add-AzureWebRole** parancsmag egy webes munkatársi szerepkört ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d24d5-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="d24d5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d24d5-109">EXAMPLES</span></span>

### <span data-ttu-id="d24d5-110">Példa 1: alapértelmezett szerepkör felvétele</span><span class="sxs-lookup"><span data-stu-id="d24d5-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="d24d5-111">Ez a parancs olyan webszerepkört hoz létre, amely a Webrole1 alapértelmezett konfigurációjának neve és egyetlen példánya.</span><span class="sxs-lookup"><span data-stu-id="d24d5-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="d24d5-112">2. példa: szerepkör felvétele névvel</span><span class="sxs-lookup"><span data-stu-id="d24d5-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="d24d5-113">A parancs hozzáadja a MyWebRole nevű egyetlen webszerepkört az aktuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="d24d5-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="d24d5-114">3. példa: szerepkör felvétele név és előfordulási számmal</span><span class="sxs-lookup"><span data-stu-id="d24d5-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="d24d5-115">A parancs hozzáadja a MyWebRole nevű webszerepkört az aktuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="d24d5-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="d24d5-116">A parancsmagban a szerepkör-példányok száma 2.</span><span class="sxs-lookup"><span data-stu-id="d24d5-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="d24d5-117">4. példa: szerepkör felvétele névvel és sablonnal</span><span class="sxs-lookup"><span data-stu-id="d24d5-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="d24d5-118">A parancs hozzáadja a MyWebRole nevű egyetlen webszerepkört az aktuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="d24d5-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="d24d5-119">A parancs az állványzat sablonként a MyWebTemplateFolder nevű mappát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d24d5-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="d24d5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d24d5-120">PARAMETERS</span></span>

### <span data-ttu-id="d24d5-121">-Példányok</span><span class="sxs-lookup"><span data-stu-id="d24d5-121">-Instances</span></span>
<span data-ttu-id="d24d5-122">A példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d24d5-122">Specifies the number of instances.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24d5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d24d5-123">-Name</span></span>
<span data-ttu-id="d24d5-124">A webes szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d24d5-124">Specifies the name of the web role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24d5-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d24d5-125">-Profile</span></span>
<span data-ttu-id="d24d5-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d24d5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d24d5-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d24d5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d24d5-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="d24d5-128">-TemplateFolder</span></span>
<span data-ttu-id="d24d5-129">A sablon mappáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d24d5-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="d24d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24d5-130">CommonParameters</span></span>
<span data-ttu-id="d24d5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d24d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24d5-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24d5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d24d5-133">INPUTS</span></span>

## <span data-ttu-id="d24d5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d24d5-134">OUTPUTS</span></span>

## <span data-ttu-id="d24d5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d24d5-135">NOTES</span></span>

## <span data-ttu-id="d24d5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d24d5-136">RELATED LINKS</span></span>

[<span data-ttu-id="d24d5-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="d24d5-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="d24d5-138">Új – AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="d24d5-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


