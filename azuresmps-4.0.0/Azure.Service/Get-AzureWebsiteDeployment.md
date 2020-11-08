---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016509"
---
# <span data-ttu-id="5b1a0-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="5b1a0-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="5b1a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1a0-103">Beolvassa a webhelyek telepített példányait.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="5b1a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b1a0-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5b1a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1a0-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5b1a0-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5b1a0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5b1a0-108">Beilleszti az Azure webhelyének telepített példányait.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="5b1a0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5b1a0-109">EXAMPLES</span></span>

## <span data-ttu-id="5b1a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b1a0-110">PARAMETERS</span></span>

### <span data-ttu-id="5b1a0-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="5b1a0-111">-CommitId</span></span>
<span data-ttu-id="5b1a0-112">A központi telepítő egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="5b1a0-113">– Részletek</span><span class="sxs-lookup"><span data-stu-id="5b1a0-113">-Details</span></span>
<span data-ttu-id="5b1a0-114">Részletes információk megjelenítése a bevezetésekről.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-114">Shows detailed information about the deployments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a0-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="5b1a0-115">-MaxResults</span></span>
<span data-ttu-id="5b1a0-116">Azt adja meg, hogy a parancs hány találatot szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1a0-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b1a0-117">-Name</span></span>
<span data-ttu-id="5b1a0-118">Annak a webhelynek a nevét adja meg, amelynek a központi telepítéséhez szükséges információkat szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="5b1a0-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b1a0-119">-Profile</span></span>
<span data-ttu-id="5b1a0-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b1a0-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b1a0-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="5b1a0-122">-Slot</span></span>
<span data-ttu-id="5b1a0-123">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b1a0-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="5b1a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1a0-124">CommonParameters</span></span>
<span data-ttu-id="5b1a0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b1a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1a0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1a0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b1a0-127">INPUTS</span></span>

## <span data-ttu-id="5b1a0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b1a0-128">OUTPUTS</span></span>

## <span data-ttu-id="5b1a0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b1a0-129">NOTES</span></span>

## <span data-ttu-id="5b1a0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b1a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="5b1a0-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="5b1a0-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


