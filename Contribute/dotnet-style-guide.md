---
title: Vorlage und Spickzettel für .NET-Artikel
description: In diesem Artikel ist eine praktische Vorlage enthalten, die Sie zum Erstellen neuer Artikel für die Repositorys der .NET-Dokumentation verwenden können.
ms.date: 11/07/2018
ms.openlocfilehash: e342373a09b623dc71aadd63e8d8627d154ec8b6
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712922"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="dc38b-103">Metadaten und Markdownvorlage für .NET-Dokumentationen</span><span class="sxs-lookup"><span data-stu-id="dc38b-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="dc38b-104">Diese dotnet/docs-Vorlage enthält Beispiele für die Markdownsyntax sowie Anweisungen zum Einstellen der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="dc38b-105">Beim Erstellen einer Markdowndatei sollten Sie die enthaltene Vorlage in eine neue Datei kopieren, die Metadaten wie unten gezeigt ausfüllen und den Titel des Artikels in der obigen H1-Überschrift festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="dc38b-106">Metadaten</span><span class="sxs-lookup"><span data-stu-id="dc38b-106">Metadata</span></span>

<span data-ttu-id="dc38b-107">Der erforderliche Metadatenblock befindet sich im folgenden Metadatenblockbeispiel:</span><span class="sxs-lookup"><span data-stu-id="dc38b-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="dc38b-108">Sie **müssen** zwischen dem Doppelpunkt („:“) und dem Wert eines Metadatenelements ein Leerzeichen setzen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="dc38b-109">Doppelpunkte in einem Wert (z.B. in einem Titel) unterbrechen den Metadatenparser.</span><span class="sxs-lookup"><span data-stu-id="dc38b-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="dc38b-110">In diesem Fall müssen Sie doppelte Anführungszeichen um den Titel setzen (z.B. `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="dc38b-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="dc38b-111">**title**: Wird in den Ergebnissen von Suchmaschinen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dc38b-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="dc38b-112">Der Titel sollte nicht mit dem Titel in Ihrer H1-Überschrift übereinstimmen und darf maximal 60 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="dc38b-113">**description**: Zusammenfassung des Artikelinhalts.</span><span class="sxs-lookup"><span data-stu-id="dc38b-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="dc38b-114">Für gewöhnlich wird diese Beschreibung in den Suchergebnissen angezeigt, jedoch wird sie nicht für die Suchrangfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc38b-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="dc38b-115">Einschließlich der Leerzeichen sollte die Länge der Beschreibung zwischen 115 und 145 Zeichen liegen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="dc38b-116">**author**: Das Feld „author“ (Autor) sollte den **GitHub-Benutzernamen** des Autors enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="dc38b-117">**ms.date**: Das Datum des letzten wichtigen Updates.</span><span class="sxs-lookup"><span data-stu-id="dc38b-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="dc38b-118">Aktualisieren Sie dieses Datum bei vorhandenen Artikeln, wenn Sie einen gesamten Artikel prüfen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="dc38b-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="dc38b-119">Kleine Fehlerbehebungen, z.B. Tippfehler oder ähnliches, rechtfertigen ein Update nicht.</span><span class="sxs-lookup"><span data-stu-id="dc38b-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="dc38b-120">An jeden Artikel werden weitere Metadaten angefügt, allerdings werden die meisten Metadatenwerte in der Regel auf der Ordnerebene angewendet. Dies wird in der Datei **docfx.json** angegeben.</span><span class="sxs-lookup"><span data-stu-id="dc38b-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="dc38b-121">Grundlegendes Markdown, GFM und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="dc38b-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="dc38b-122">Die Grundlagen von Markdown, GFM (GitHub Flavored Markdown) und OPS-spezifischen Erweiterungen können Sie anhand des allgemeinen Artikels zu [Markdown](how-to-write-use-markdown.md) und der [Markdownreferenz](markdown-reference.md) erlernen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="dc38b-123">Markdown nutzt Sonderzeichen wie \*, \` und \# für die Formatierung.</span><span class="sxs-lookup"><span data-stu-id="dc38b-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="dc38b-124">Wenn Sie eines dieser Zeichen in Ihren Inhalt einfügen möchten, müssen Sie eine der folgenden Vorgehensweisen anwenden:</span><span class="sxs-lookup"><span data-stu-id="dc38b-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="dc38b-125">Versehen Sie das Sonderzeichen mit einem umgekehrten Schrägstrich als Escapezeichen (z.B. `\*` für \*).</span><span class="sxs-lookup"><span data-stu-id="dc38b-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="dc38b-126">Verwenden Sie den [HTML-Code](http://www.ascii.cl/htmlcodes.htm) für das Zeichen (z.B. `&#42;` für &#42;).</span><span class="sxs-lookup"><span data-stu-id="dc38b-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="dc38b-127">Dateinamen</span><span class="sxs-lookup"><span data-stu-id="dc38b-127">File names</span></span>

<span data-ttu-id="dc38b-128">Dateinamen unterliegen folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="dc38b-128">File names use the following rules:</span></span>

* <span data-ttu-id="dc38b-129">Nur Kleinbuchstaben, Zahlen und Bindestriche sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="dc38b-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="dc38b-130">Leer- oder Satzzeichen sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="dc38b-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="dc38b-131">Worte und Zahlen im Dateinamen werden durch Bindestriche getrennt.</span><span class="sxs-lookup"><span data-stu-id="dc38b-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="dc38b-132">Verwenden Sie Verben, die den Zweck angeben, z.B. develop, buy, build, troubleshoot.</span><span class="sxs-lookup"><span data-stu-id="dc38b-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="dc38b-133">Auf „-ing“ endenden Worte dürfen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc38b-133">No -ing words.</span></span>
* <span data-ttu-id="dc38b-134">Kurze Worte wie a, and, the, in, or usw. sind nicht erlaubt.</span><span class="sxs-lookup"><span data-stu-id="dc38b-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="dc38b-135">Das Markdownformat und die Erweiterung „.md“ sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc38b-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="dc38b-136">Verwenden Sie angemessene, kurze Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-136">Keep file names reasonably short.</span></span> <span data-ttu-id="dc38b-137">Sie sind Teil der URL für Ihre Artikel.</span><span class="sxs-lookup"><span data-stu-id="dc38b-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="dc38b-138">Überschriften</span><span class="sxs-lookup"><span data-stu-id="dc38b-138">Headings</span></span>

<span data-ttu-id="dc38b-139">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="dc38b-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="dc38b-140">Schreiben Sie das erste Wort einer Überschrift immer groß.</span><span class="sxs-lookup"><span data-stu-id="dc38b-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="dc38b-141">Textformatierung</span><span class="sxs-lookup"><span data-stu-id="dc38b-141">Text styling</span></span>

<span data-ttu-id="dc38b-142">*Kursiv:* Für Dateien, Ordner, Pfade (für lange Elemente, die in Ihre eigene Zeile getrennt werden) und neue Begriffe</span><span class="sxs-lookup"><span data-stu-id="dc38b-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="dc38b-143">**Fett:** Für Benutzeroberflächenelemente</span><span class="sxs-lookup"><span data-stu-id="dc38b-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="dc38b-144">`Code` für Inlinecode, Schlüsselwörter der Sprache, NuGet-Paketnamen, Befehlszeilenbefehle, Datenbanktabellen- und Spaltennamen sowie URLs, die nicht klickbar sein sollen</span><span class="sxs-lookup"><span data-stu-id="dc38b-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="dc38b-145">Links</span><span class="sxs-lookup"><span data-stu-id="dc38b-145">Links</span></span>

<span data-ttu-id="dc38b-146">Informationen zu Ankern, internen Links, Links zu anderen Dokumenten, Codeeinfügungen und externen Links finden Sie im allgemeinen Artikel zu [Links](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="dc38b-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="dc38b-147">Das Team für die .NET-Dokumentation wendet folgende Konventionen an:</span><span class="sxs-lookup"><span data-stu-id="dc38b-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="dc38b-148">In den meisten Fällen werden relative Links verwendet. Von der Verwendung von `~/` wird in Links abgeraten, weil relative Links zur Quelle auf GitHub führen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="dc38b-149">Allerdings wird das Zeichen `~/` für Links zu Dateien in abhängigen Repositorys verwendet, um den Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc38b-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="dc38b-150">Da die Dateien im abhängigen Repository sich auf GitHub an einem anderen Speicherort befinden, werden die Links mit relativen Links, unabhängig davon, wie sie geschrieben sind, nicht richtig aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc38b-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="dc38b-151">Die C#-Sprachspezifikation und die Visual Basic-Sprachspezifikation sind in den .NET-Dokumentationen enthalten, indem die Quelle der Sprach-Repositorys eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="dc38b-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="dc38b-152">Die Markdownquellen werden in den Repositorys [csharplang](https://github.com/dotnet/csharplang) und [vblang](https://github.com/dotnet/vblang) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dc38b-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="dc38b-153">Links zu den Sprachspezifikationen müssen zu den Quellverzeichnissen zeigen, in denen diese Spezifikationen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dc38b-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="dc38b-154">Für C# ist das Verzeichnis **~/_csharplang/spec**, und für Visual Basic ist das Verzeichnis **~/_vblang/spec**. Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="dc38b-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="dc38b-155">Links zu APIs</span><span class="sxs-lookup"><span data-stu-id="dc38b-155">Links to APIs</span></span>

<span data-ttu-id="dc38b-156">Das Buildsystem verfügt über einige Erweiterungen, mit denen Sie Links zu .NET-APIs erstellen können, ohne externe Links verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="dc38b-157">Verwenden Sie eine der folgenden Syntaxvarianten:</span><span class="sxs-lookup"><span data-stu-id="dc38b-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="dc38b-158">Automatische Verknüpfung: `<xref:UID>` oder `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="dc38b-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="dc38b-159">Der `displayProperty`-Abfrageparameter erzeugt einen vollqualifizierten Linktext.</span><span class="sxs-lookup"><span data-stu-id="dc38b-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="dc38b-160">Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an.</span><span class="sxs-lookup"><span data-stu-id="dc38b-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="dc38b-161">Markdownlink: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="dc38b-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="dc38b-162">Verwenden Sie den Markdownlink, wenn Sie den angezeigten Linktext anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="dc38b-163">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="dc38b-163">Examples:</span></span>

- <span data-ttu-id="dc38b-164">`<xref:System.String>` wird als [Zeichenfolge](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="dc38b-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="dc38b-165">`<xref:System.String?displayProperty=nameWithType>` wird als [System.String](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="dc38b-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="dc38b-166">`[String class](xref:System.String)` wird als [Zeichenfolgenklasse](https://docs.microsoft.com/dotnet/api/system.string) gerendert</span><span class="sxs-lookup"><span data-stu-id="dc38b-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="dc38b-167">Weitere Informationen zur Verwendung dieser Notation finden Sie unter [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference) (Verwenden des Querverweises).</span><span class="sxs-lookup"><span data-stu-id="dc38b-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="dc38b-168">Wenn die UID die Sonderzeichen \`, \# oder \* enthält, muss der UID-Wert jeweils als `%60`, `%23` und `%2A` im HTML-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="dc38b-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="dc38b-169">Manchmal sehen Sie die Codierung mit Klammern, aber dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc38b-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="dc38b-170">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="dc38b-170">Examples:</span></span>

- <span data-ttu-id="dc38b-171">System.Threading.Tasks.Task\`1 wird `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="dc38b-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="dc38b-172">System.Exception.\#ctor wird `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="dc38b-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="dc38b-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) wird `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="dc38b-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="dc38b-174">Die UIDs von Typen, eine Liste von überladenen Membern oder einen bestimmten überladenen Member finden Sie über `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="dc38b-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="dc38b-175">Die Abfragezeichenfolge `?text=*\<type-member-name>*` gibt den Typ oder Member an, dessen UIDs Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="dc38b-176">`https://xref.docs.microsoft.com/autocomplete?text=string.format` ruft beispielsweise die Überladungen [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) ab.</span><span class="sxs-lookup"><span data-stu-id="dc38b-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="dc38b-177">Das Tool sucht in der UID nach dem angegebenen Abfrageparameter `text`.</span><span class="sxs-lookup"><span data-stu-id="dc38b-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="dc38b-178">Zum Beispiel können Sie nach Membernamen (ToString), partiellen Membernamen (ToStri), Typen und Membernamen (Double.ToString) und mehr suchen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="dc38b-179">Wenn Sie \* (oder `%2A`) hinter der UID hinzufügen, steht der Link für die Überladungsseite und nicht für eine bestimmte API.</span><span class="sxs-lookup"><span data-stu-id="dc38b-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="dc38b-180">Dies können Sie z.B. verwenden, wenn Sie eine Verknüpfung mit der Seite [List\<T>.BinarySearch-Methode](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) auf generische Weise als Alternative zu einer bestimmten Überladung wie [List\<T>.BinarySearch (T, IComparer\<T >)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="dc38b-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="dc38b-181">Sie können auch \* verwenden, um einen Link zu einer Memberseite zu erstellen, wenn der Member nicht überladen ist. Damit ersparen Sie sich das Einfügen der Parameterliste in die UID.</span><span class="sxs-lookup"><span data-stu-id="dc38b-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="dc38b-182">Sie müssen den vollqualifizierten Namen des Typs jedes Parameters der Methode einfügen, um einen Link zu einer spezifischen Methodenüberladung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="dc38b-183">Zum Beispiel führt \<xref:System.DateTime.ToString> zu der parameterlosen Methode [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), und \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> führt zu der Methode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="dc38b-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="dc38b-184">Verwenden Sie zum Verknüpfen eines generischen Typs (z.B. [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)) das Zeichen \` (`%60`) gefolgt von der Anzahl generischer Typparameter.</span><span class="sxs-lookup"><span data-stu-id="dc38b-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="dc38b-185">Zum Beispiel verknüpft `<xref:System.Nullable%601>` den Typ [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), und `<xref:System.Func%602>` verknüpft den Delegaten [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="dc38b-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="dc38b-186">Code</span><span class="sxs-lookup"><span data-stu-id="dc38b-186">Code</span></span>

<span data-ttu-id="dc38b-187">Die beste Methode zum Einfügen von Code besteht darin, Ausschnitte aus einem funktionstüchtigen Beispiel einzufügen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="dc38b-188">Erstellen Sie Ihr Beispiel anhand der Anweisungen im Artikel [Contributing to .NET (Mitwirken an .NET)](dotnet-contribute-process.md#contributing-to-samples).</span><span class="sxs-lookup"><span data-stu-id="dc38b-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="dc38b-189">Die grundlegenden Regeln zum Einfügen von Code finden Sie im allgemeinen Leitfaden für [Code](how-to-write-use-markdown.md#code-snippets).</span><span class="sxs-lookup"><span data-stu-id="dc38b-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="dc38b-190">Sie können den Code mithilfe der folgenden Syntax einfügen:</span><span class="sxs-lookup"><span data-stu-id="dc38b-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="dc38b-191">`-<language>` (*optional*, aber *empfohlen*)</span><span class="sxs-lookup"><span data-stu-id="dc38b-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="dc38b-192">Sprache des referenzierten Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="dc38b-192">Language of the code snippet being referenced.</span></span> <span data-ttu-id="dc38b-193">Eine Liste der unterstützten Werte finden Sie unter [Supported languages (Unterstützte Sprachen)](#supported-languages).</span><span class="sxs-lookup"><span data-stu-id="dc38b-193">For a list of supported values, see [Supported languages](#supported-languages).</span></span>

* <span data-ttu-id="dc38b-194">`<name>` (*optional*)</span><span class="sxs-lookup"><span data-stu-id="dc38b-194">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="dc38b-195">Name des Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="dc38b-195">Name for the code snippet.</span></span> <span data-ttu-id="dc38b-196">Er wirkt sich nicht auf die HTML-Ausgabe aus, Sie können ihn jedoch verwenden, um die Lesbarkeit Ihrer Markdownquelle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="dc38b-196">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="dc38b-197">`<pathToFile>` (*obligatorisch*)</span><span class="sxs-lookup"><span data-stu-id="dc38b-197">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="dc38b-198">Relativer Pfad im Dateisystem, der die Codeausschnittdatei angibt, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dc38b-198">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="dc38b-199">Dies kann sich aufgrund der verschiedenen Repositorys, aus denen die .NET-Dokumentation besteht, als kompliziert erweisen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-199">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="dc38b-200">Die .NET-Beispiele befinden sich im Repository „dotnet/samples“.</span><span class="sxs-lookup"><span data-stu-id="dc38b-200">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="dc38b-201">Alle Pfade für Codeausschnitte beginnen mit `~/samples`, der Rest ist der Pfad vom Stamm zur Quelle des Repositorys.</span><span class="sxs-lookup"><span data-stu-id="dc38b-201">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="dc38b-202">`<queryoption>` (*optional*)</span><span class="sxs-lookup"><span data-stu-id="dc38b-202">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="dc38b-203">Wird verwendet, um anzugeben, wie der Code aus der Datei abgerufen werden soll:</span><span class="sxs-lookup"><span data-stu-id="dc38b-203">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="dc38b-204">`#`: `#{tagname}` (Tagname) *oder*`#L{startlinenumber}-L{endlinenumber}` (Zeilenbereich).</span><span class="sxs-lookup"><span data-stu-id="dc38b-204">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="dc38b-205">Von der Verwendung von Zeilennummern wird abgeraten, da sie sehr fehleranfällig sind.</span><span class="sxs-lookup"><span data-stu-id="dc38b-205">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="dc38b-206">Zum Referenzieren von Codeausschnitten werden Tagnamen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-206">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="dc38b-207">Verwenden Sie aussagekräftige Tagnamen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-207">Use meaningful tag names.</span></span> <span data-ttu-id="dc38b-208">(Viele Codeausschnitte wurden aus einer vorherigen Plattform migriert, und die Tags haben Namen wie `Snippet1`, `Snippet2` usw. Diese Vorgehensweise ist weitaus schwerer zu verwalten.)</span><span class="sxs-lookup"><span data-stu-id="dc38b-208">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="dc38b-209">`range`: `?range=1,3-5` Ein Bereich von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-209">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="dc38b-210">Dieses Beispiel enthält die Zeilen 1, 3, 4 und 5.</span><span class="sxs-lookup"><span data-stu-id="dc38b-210">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="dc38b-211">Es wird empfohlen, wenn möglich die Option zum Benennen der Tags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc38b-211">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="dc38b-212">Der Tagname ist der Name eines Bereichs oder eines Codekommentars im im Quellcode enthaltenen Format `Snippettagname`.</span><span class="sxs-lookup"><span data-stu-id="dc38b-212">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="dc38b-213">Im folgenden Beispiel wird veranschaulicht, wie der Tagname `BasicThrow` referenziert wird:</span><span class="sxs-lookup"><span data-stu-id="dc38b-213">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="dc38b-214">Der relative Pfad zur Quelle im Repository **dotnet/samples** folgt dem Pfad `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="dc38b-214">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="dc38b-215">In [dieser Quelldatei](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) wird dargestellt, wie Tags von Ausschnitten strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="dc38b-215">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="dc38b-216">Details zur Darstellung des Tagnamens in den Quelldateien des Codeausschnitts pro Sprache finden Sie unter [DocFX-Richtlinien](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="dc38b-216">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="dc38b-217">Im folgenden Beispiel wird Code in allen drei .NET-Sprachen gezeigt:</span><span class="sxs-lookup"><span data-stu-id="dc38b-217">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="dc38b-218">Durch Einfügen von Ausschnitten aus vollständigen Programmen wird sichergestellt, dass der gesamte Code das CI-System (Continuous Integration) durchläuft.</span><span class="sxs-lookup"><span data-stu-id="dc38b-218">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="dc38b-219">Wenn Sie jedoch etwas veranschaulichen müssen, das zu Fehlern zur Kompilier- oder Laufzeit führt, können Sie Inlinecodeblöcke verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc38b-219">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="dc38b-220">Bilder</span><span class="sxs-lookup"><span data-stu-id="dc38b-220">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="dc38b-221">Statisches Bild oder animiertes GIF</span><span class="sxs-lookup"><span data-stu-id="dc38b-221">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="dc38b-222">Verknüpftes Bild</span><span class="sxs-lookup"><span data-stu-id="dc38b-222">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="dc38b-223">Videos</span><span class="sxs-lookup"><span data-stu-id="dc38b-223">Videos</span></span>

<span data-ttu-id="dc38b-224">Derzeit können Sie mithilfe der folgenden Syntax sowohl Channel 9- als auch YouTube-Videos einbetten:</span><span class="sxs-lookup"><span data-stu-id="dc38b-224">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="dc38b-225">Channel 9</span><span class="sxs-lookup"><span data-stu-id="dc38b-225">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="dc38b-226">Wählen Sie die Registerkarte **Embed** (Einbetten) unter dem Video aus, und kopieren Sie die URL aus dem `<iframe>`-Element, um die richtige URL des Videos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-226">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="dc38b-227">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dc38b-227">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="dc38b-228">YouTube</span><span class="sxs-lookup"><span data-stu-id="dc38b-228">YouTube</span></span>

<span data-ttu-id="dc38b-229">Klicken Sie mit der rechten Maustaste auf das Video, und wählen Sie **Einbettungscode kopieren** aus `<iframe>`, um die richtige URL des Videos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dc38b-229">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="dc38b-230">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dc38b-230">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="dc38b-231">Erweiterungen für docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="dc38b-231">docs.microsoft extensions</span></span>

<span data-ttu-id="dc38b-232">Einige zusätzliche Erweiterungen für GitHub Flavored Markdown werden von docs.microsoft bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dc38b-232">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="dc38b-233">Listen mit Häkchen</span><span class="sxs-lookup"><span data-stu-id="dc38b-233">Checked lists</span></span>

<span data-ttu-id="dc38b-234">Für Listen ist eine benutzerdefinierte Formatvorlage verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc38b-234">A custom style is available for lists.</span></span> <span data-ttu-id="dc38b-235">Sie können Listen mit grünen Häkchen ausgeben.</span><span class="sxs-lookup"><span data-stu-id="dc38b-235">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="dc38b-236">Dies wird wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="dc38b-236">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="dc38b-237">Erstellen einer .NET Core-App</span><span class="sxs-lookup"><span data-stu-id="dc38b-237">How to create a .NET Core app</span></span>
> * <span data-ttu-id="dc38b-238">Hinzufügen eines Verweises zum Microsoft.XmlSerializer.Generator-Paket</span><span class="sxs-lookup"><span data-stu-id="dc38b-238">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="dc38b-239">Bearbeiten Ihrer MyApp.csproj-Datei zum Hinzufügen von Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="dc38b-239">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="dc38b-240">Hinzufügen von „XmlSerializer“ und einer Klasse</span><span class="sxs-lookup"><span data-stu-id="dc38b-240">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="dc38b-241">Erstellen und Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="dc38b-241">How to build and run the application</span></span>

<span data-ttu-id="dc38b-242">Ein Beispiel der Liste mit Häkchen finden Sie in dieser [.NET Core-Dokumentation](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="dc38b-242">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="dc38b-243">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="dc38b-243">Buttons</span></span>

<span data-ttu-id="dc38b-244">Schaltflächenlinks:</span><span class="sxs-lookup"><span data-stu-id="dc38b-244">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="dc38b-245">Dies wird wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="dc38b-245">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="dc38b-246">Schaltflächenlinks</span><span class="sxs-lookup"><span data-stu-id="dc38b-246">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="dc38b-247">Ein Beispiel solcher Schaltflächen finden Sie in dieser [Visual Studio-Dokumentation](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="dc38b-247">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="dc38b-248">Exemplarische Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="dc38b-248">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="dc38b-249">Ein Beispiel für exemplarische Vorgehensweisen finden Sie in diesem [C#-Leitfaden](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="dc38b-249">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>