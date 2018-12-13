---
title: Az Azure PowerShell Az modul bemutatása
description: Bemutatkozik az új Azure PowerShell-modul, az Az, amely az AzureRM modult váltja le.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217541"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="01028-103">Az új Azure PowerShell Az modul bemutatása</span><span class="sxs-lookup"><span data-stu-id="01028-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="01028-104">2018 novemberétől az Azure PowerShell `Az` modul teljes nyilvános előzetes verzióban érhető el</span><span class="sxs-lookup"><span data-stu-id="01028-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="01028-105">Az Az rövidebb parancsokat és nagyobb stabilitást kínál, továbbá a Windows, macOS és Linux rendszert egyaránt támogatja.</span><span class="sxs-lookup"><span data-stu-id="01028-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="01028-106">Emellett funkcióparitást és egyszerű áttelepítési útvonalat biztosít az AzureRM-ről.</span><span class="sxs-lookup"><span data-stu-id="01028-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="01028-107">Az Az a .NET Standard-kódtárat használja, ami azt jelenti, hogy fut a PowerShell 5.x és PowerShell 6.x verziókon is.</span><span class="sxs-lookup"><span data-stu-id="01028-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="01028-108">Mivel a PowerShell 6.x a Linux, a macOS és a Windows alatt egyaránt képes futni, ez azt jelenti, hogy az Az minden platformon elérhető.</span><span class="sxs-lookup"><span data-stu-id="01028-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="01028-109">A .NET Standard használatával az Azure PowerShell kódbázisa egységesíthető, és mindez csak minimális hatással van a felhasználókra.</span><span class="sxs-lookup"><span data-stu-id="01028-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="01028-110">Az Az egy új modul, ezért a verziószámozás vissza lett állítva.</span><span class="sxs-lookup"><span data-stu-id="01028-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="01028-111">Az első stabil kiadás az 1.0 lesz, de a modul 2018 novemberétől biztosítja a funkcióparitást az AzureRm-mel.</span><span class="sxs-lookup"><span data-stu-id="01028-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="01028-112">Frissítés az Az modulra</span><span class="sxs-lookup"><span data-stu-id="01028-112">Upgrade to Az</span></span>

<span data-ttu-id="01028-113">Javasoljuk, hogy a felhasználók frissítsenek az új `Az` modulra.</span><span class="sxs-lookup"><span data-stu-id="01028-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="01028-114">Ehhez tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="01028-114">To do so:</span></span>

* [<span data-ttu-id="01028-115">Távolítsa el az Azure PowerShell AzureRM modult.</span><span class="sxs-lookup"><span data-stu-id="01028-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="01028-116">Telepítse az Azure PowerShell Az modult.</span><span class="sxs-lookup"><span data-stu-id="01028-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="01028-117">Engedélyezze a kompatibilitási módot az AzureRM-hez az `Enable-AzureRMAlias` paranccsal, amíg meg nem ismeri az új parancskészletet.</span><span class="sxs-lookup"><span data-stu-id="01028-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="01028-118">Meglévő szkriptek áttelepítése az Az modulba</span><span class="sxs-lookup"><span data-stu-id="01028-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="01028-119">A jelentősebb frissítések kényelmetlenek tudnak lenni.</span><span class="sxs-lookup"><span data-stu-id="01028-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="01028-120">Az `Az` modul kompatibilitási módjával azonban továbbra is használhatja a meglévő szkripteket, miközben az új szintaxis frissítésein dolgozik.</span><span class="sxs-lookup"><span data-stu-id="01028-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="01028-121">Az `Enable-AzureRmAlias` parancsmaggal engedélyezheti az `AzureRM`-kompatibilitási módot.</span><span class="sxs-lookup"><span data-stu-id="01028-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="01028-122">Ez a parancsmag az `AzureRM`-parancsmagneveket az új `Az`-parancsmagnevek aliasaiként definiálja.</span><span class="sxs-lookup"><span data-stu-id="01028-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="01028-123">Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek.</span><span class="sxs-lookup"><span data-stu-id="01028-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="01028-124">A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható.</span><span class="sxs-lookup"><span data-stu-id="01028-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="01028-125">Például a régi `New-AzureRmVm` parancs megfelelője a `New-AzVm` parancs lett.</span><span class="sxs-lookup"><span data-stu-id="01028-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="01028-126">Az áttelepítési folyamat teljes leírását [az AzureRM modulból az Az modulba való áttelepítést ismertető szakaszban találja](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="01028-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="01028-127">Az AzureRM jövőbeli támogatottsága</span><span class="sxs-lookup"><span data-stu-id="01028-127">The future of support for AzureRM</span></span>

<span data-ttu-id="01028-128">Az `Az` 1.0-s verziójának 2018 decemberi kiadásával a meglévő `AzureRM` modul nem bővül majd újabb parancsmagokkal vagy funkciókkal.</span><span class="sxs-lookup"><span data-stu-id="01028-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="01028-129">Azonban az `AzureRM` hivatalos karbantartása és hibajavítása nem szűnik meg.</span><span class="sxs-lookup"><span data-stu-id="01028-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="01028-130">Az Azure legfrissebb szolgáltatásainak és funkcióinak használatához érdemes áttérnie az `Az` modul használatára.</span><span class="sxs-lookup"><span data-stu-id="01028-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>