---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015598"
---
# <span data-ttu-id="d5f13-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="d5f13-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="d5f13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5f13-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f13-103">A szerepkörben való telepítéshez elérhető futtatókörnyezetek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d5f13-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="d5f13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5f13-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5f13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5f13-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f13-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d5f13-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d5f13-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d5f13-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d5f13-108">Elérhetővé válik a szerepkörben telepítendő futtatókörnyezetek.</span><span class="sxs-lookup"><span data-stu-id="d5f13-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="d5f13-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5f13-109">EXAMPLES</span></span>

## <span data-ttu-id="d5f13-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5f13-110">PARAMETERS</span></span>

### <span data-ttu-id="d5f13-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5f13-111">-Profile</span></span>
<span data-ttu-id="d5f13-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d5f13-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5f13-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d5f13-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5f13-114">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="d5f13-114">-Runtime</span></span>
<span data-ttu-id="d5f13-115">A futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="d5f13-115">The name of the runtime.</span></span>
<span data-ttu-id="d5f13-116">Ha egy futásidejű érték van megadva, akkor csak az adott futásidejű verziót lehet telepíteni a Windows Azure szerepkörében.</span><span class="sxs-lookup"><span data-stu-id="d5f13-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="d5f13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f13-117">CommonParameters</span></span>
<span data-ttu-id="d5f13-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5f13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f13-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f13-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f13-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f13-120">INPUTS</span></span>

## <span data-ttu-id="d5f13-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f13-121">OUTPUTS</span></span>

## <span data-ttu-id="d5f13-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5f13-122">NOTES</span></span>

## <span data-ttu-id="d5f13-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5f13-123">RELATED LINKS</span></span>

[<span data-ttu-id="d5f13-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="d5f13-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="d5f13-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="d5f13-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="d5f13-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="d5f13-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="d5f13-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d5f13-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


