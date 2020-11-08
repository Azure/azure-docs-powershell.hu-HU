---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015463"
---
# <span data-ttu-id="54410-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="54410-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="54410-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54410-102">SYNOPSIS</span></span>
<span data-ttu-id="54410-103">Egy webhely előző telepített példányának újratelepítése az Azure-ban</span><span class="sxs-lookup"><span data-stu-id="54410-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="54410-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54410-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54410-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54410-105">DESCRIPTION</span></span>
<span data-ttu-id="54410-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="54410-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="54410-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="54410-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="54410-108">A **Restore-AzureWebsiteDeployment** parancsmag áttelepíti az Azure-webhely korábbi telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="54410-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="54410-109">Ez a folyamat lecseréli az aktuális telepítést a kijelölt telepítéssel.</span><span class="sxs-lookup"><span data-stu-id="54410-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="54410-110">Példák</span><span class="sxs-lookup"><span data-stu-id="54410-110">EXAMPLES</span></span>

### <span data-ttu-id="54410-111">1. példa: webhely újratelepítése</span><span class="sxs-lookup"><span data-stu-id="54410-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="54410-112">Ez a parancs áttelepíti a ContosoSite nevű webhely azonosító f876543210 tartalmazó példányát.</span><span class="sxs-lookup"><span data-stu-id="54410-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="54410-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54410-113">PARAMETERS</span></span>

### <span data-ttu-id="54410-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="54410-114">-CommitId</span></span>
<span data-ttu-id="54410-115">Az újratelepítéshez használt központi telepítés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="54410-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="54410-116">-Force</span><span class="sxs-lookup"><span data-stu-id="54410-116">-Force</span></span>
<span data-ttu-id="54410-117">Ha engedélyezve van, a program újratelepíti az előző telepítést a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="54410-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="54410-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54410-118">-Name</span></span>
<span data-ttu-id="54410-119">Annak a webhelynek a neve, ahová a rendszert át szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="54410-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="54410-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="54410-120">-Profile</span></span>
<span data-ttu-id="54410-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="54410-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54410-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="54410-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54410-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="54410-123">-Slot</span></span>
<span data-ttu-id="54410-124">A bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54410-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="54410-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54410-125">-Confirm</span></span>
<span data-ttu-id="54410-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54410-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54410-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54410-127">-WhatIf</span></span>
<span data-ttu-id="54410-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54410-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54410-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54410-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54410-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54410-130">CommonParameters</span></span>
<span data-ttu-id="54410-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54410-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54410-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54410-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54410-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54410-133">INPUTS</span></span>

## <span data-ttu-id="54410-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54410-134">OUTPUTS</span></span>

## <span data-ttu-id="54410-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54410-135">NOTES</span></span>

## <span data-ttu-id="54410-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54410-136">RELATED LINKS</span></span>

[<span data-ttu-id="54410-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="54410-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="54410-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="54410-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


